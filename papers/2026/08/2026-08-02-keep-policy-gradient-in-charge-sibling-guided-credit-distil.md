---
title: "Keep Policy Gradient in Charge: Sibling-Guided Credit Distillation for Long-Horizon Tool-Use Agents"
authors: ["Tianyu Ding", "Jianhong Xin", "Juan Pablo De la Cruz Weinstein"]
date: 2026-06-10
arxiv_id: "2606.12634"
url: "https://arxiv.org/abs/2606.12634"
score: 0.81
topics: [agentic RL, tool use, GRPO, LLM agent]
status: unread
---

# Keep Policy Gradient in Charge: Sibling-Guided Credit Distillation for Long-Horizon Tool-Use Agents

## Summary

SGCD (Sibling-Guided Credit Distillation) uses dynamic sampling to produce mixed successful/failed sibling rollouts on the same task, then has an external LLM contrast them to produce a training-only credit reference that reshapes GRPO token advantages via detached teacher/student divergence. Critically, the deployed student receives only the clean task prompt — the credit reference is training-only, preventing teacher dependency. On AppWorld and tau^3-airline, SGCD improves over GRPO-family baselines with gains of 2.7 points on AppWorld test_challenge.

## Key Contributions

- **Sibling-rollout contrast via external LLM**: success/fail pairs on same task → structured credit summary → token-advantage reshaping; credit is derived from the task verifier (not a fixed teacher model)
- **Detached divergence for reshaping**: teacher/student KL with stop-gradient prevents the distillation from overriding the policy gradient signal — the design principle that prior direct self-distillation papers (including GRSD) failed to enforce
- **Training-only credit reference**: deployed model is clean-prompt only; architectural dependency on an external LLM is isolated to training, not inference
- **Results on AppWorld**: test_normal TGC 42.9→45.6, test_challenge 24.7→27.0 over GRPO baseline

## Relevance

SGCD is structurally related to GRSD (Jul 31 vault, within-group NL reflection for contrastive credit) but operates across sibling rollouts rather than within-group trajectories, and uses an external LLM rather than the policy's own reflection. Together they define a new dimension in the credit-source taxonomy: (a) within-group statistical contrast (STARE, ERPO) → (b) within-group NL reflection (GRSD) → (c) cross-sibling NL contrast (SGCD). The "keep policy gradient in charge" design rule is also related to A²TGPO's stop-gradient accumulation mechanism, but applied to the distillation channel rather than the IG normalization channel.

## My Thoughts

<!-- Add your own notes here -->
