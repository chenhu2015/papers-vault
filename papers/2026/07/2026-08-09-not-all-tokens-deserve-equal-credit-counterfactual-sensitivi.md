---
title: "Not All Tokens Deserve Equal Credit: Counterfactual Sensitivity Credit Reallocation for Long-CoT Reasoning"
authors: ["Qiangqiang He", "Zhongheng Wu", "ZiJian Wang"]
date: 2026-08-09
arxiv_id: "2607.27888"
url: "https://arxiv.org/abs/2607.27888"
score: 0.85
topics: [GRPO, reward model, RLHF, agentic RL, RL training]
status: unread
---

# Not All Tokens Deserve Equal Credit: Counterfactual Sensitivity Credit Reallocation for Long-CoT Reasoning

## Summary

CSCR diagnoses OPSD's privileged shifts by fixing trajectories and re-scoring under opposing outcome conditions: most shifts fail to reverse direction and concentrate on surface-form rather than reasoning-content tokens, showing privileged signals reflect counterfactual sensitivity not learning value. CSCR reduces credit for highly sensitive tokens in GRPO and renormalizes advantages to preserve the credit budget and verifier-determined direction, consistently outperforming GRPO on long-CoT math benchmarks.

## Key Contributions

- Counterfactual test: fixing a trajectory and re-scoring under both "correct" and "incorrect" conditions reveals that most OPSD privileged shifts are insensitive to the actual outcome condition — they move in the same direction regardless
- Surface-concentration finding: large OPSD shifts concentrate on substitutable surface-form tokens; reasoning-content tokens are less sensitive, meaning the teacher signal is noisiest where it should be most informative
- CSCR algorithm: extends GRPO by downweighting tokens with high counterfactual sensitivity scores and renormalizing advantages to preserve both the total credit budget and the verifier-determined direction
- Ablation shows moderate downweighting is optimal; strong modulation destabilizes optimization

## Relevance

CSCR adds a **counterfactual robustness axis** to the vault's token-level credit taxonomy — orthogonal to all four existing axes (DASH's divergence-sequence history, PCSD's temporal persistence, OCSD's scaffold isolation, RP-OPSD's token-type detection). Where those axes ask *how* to weight the teacher's signal, CSCR asks whether the teacher's direction is reliable at all, using counterfactual outcome conditioning as the test. This directly challenges a foundational assumption of OPSD and extends the Gap #19/20 credit calibration literature to the reliability-of-direction axis.

## My Thoughts

<!-- Add your own notes here -->
