---
title: "Hints, Critics, and Teachers: Prior Injection for Sparse-Reward RL in Vision-Language Math Reasoning"
authors: ["Qiqian Fu"]
date: 2026-08-30
arxiv_id: "2608.21811"
url: "https://arxiv.org/abs/2608.21811"
score: 0.90
topics: [VLM, multimodal, GRPO, reward model, RL training, vision-language]
status: unread
---

# Hints, Critics, and Teachers: Prior Injection for Sparse-Reward RL in Vision-Language Math Reasoning

## Summary

Trains eleven prior-injection methods under identical conditions on a 20,830-problem visual-math pool where the baseline Qwen2-VL-2B answers only 3.6% of GRPO rollouts correctly, covering text hints (reference-solution injection), on-policy distillation from a 7B teacher, and value critics with MSE vs. HL-Gauss categorical loss. The central finding is that replacing the MSE critic loss with HL-Gauss cross-entropy yields +14.4 points in-domain, and that hint gains come from hint-guided exploration rather than the auxiliary UFT loss. Critically, one commonly used in-domain evaluation slice anti-correlates with genuine cross-domain transfer (Spearman rho = -0.74, n=11, permutation p=0.011), while the hardest in-domain slice predicts it closely (rho = +0.89, p<0.001), exposing a systematic measurement artifact in VLM-RL benchmarking.

## Key Contributions

- First systematic 11-arm comparison of prior injection strategies for VLM RL under near-total reward sparsity (85–97% rollout groups entirely wrong, contributing zero gradient)
- HL-Gauss categorical critic loss outperforms MSE critic by +14.4 pts in-domain with better cross-domain transfer
- Hint-guided exploration (not UFT auxiliary loss) is the mechanism driving text-hint gains — disentangles two confounded contributions
- Evaluation artifact: one standard in-domain slice anti-correlates with cross-domain transfer, warns against using it as a general-distribution check

## Relevance

The systematic multi-arm comparison directly addresses the VLM + GRPO + reward model intersection from the interest profile; the HL-Gauss critic finding is actionable for anyone building value-function components for VLM RL. The evaluation artifact warning is especially important given that several recent vault papers (MAPO, SPyCE, Visual-OPSD) use overlapping VLM-RL benchmark setups without discussing this measurement confound.

## My Thoughts

<!-- Add your own notes here -->
