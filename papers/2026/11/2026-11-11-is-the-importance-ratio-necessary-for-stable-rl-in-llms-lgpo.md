---
title: "Is the Importance Ratio Necessary for Stable Reinforcement Learning in LLMs?"
authors: ["Shuibai Zhang", "Junhyuck Kim", "Gyeongman Kim", "Jaewoong Cho"]
date: 2026-11-11
arxiv_id: "2611.15404v1"
url: "https://arxiv.org/abs/2611.15404"
score: 0.82
topics: [RL training, GRPO, RLVR, reinforcement learning]
status: unread
---

# Is the Importance Ratio Necessary for Stable Reinforcement Learning in LLMs?

## Summary

LGPO (Likelihood-Gated Policy Optimization) challenges the necessity of importance sampling ratios in GRPO, showing that removing the IS correction does not harm stability while removing the trust region causes collapse — and that ratio-based clipping is inert in fully on-policy training (ratio stays at 1). It replaces ratio-based clipping with a soft likelihood-based trust region gate, reducing training time by ~18% while remaining stable in fully on-policy regimes where standard GRPO fails. This reframes GRPO mechanics: the trust region is load-bearing, but the importance ratio itself is not.

## Key Contributions

- Empirically separates two components of GRPO: the importance sampling ratio correction and the trust region constraint — only the latter is necessary for stability
- Identifies a critical failure of ratio-based clipping in fully on-policy training: the ratio is identically 1, so the clipping constraint never activates
- Proposes LGPO: likelihood-based gating that enforces a soft trust region without computing old-policy likelihoods, saving ~18% training time
- LGPO remains stable in fully on-policy regimes where standard GRPO collapses, enabling more efficient and robust LLM RL post-training

## Relevance

This is a foundational mechanics paper for the GRPO training dynamics thread — it proves that the importance ratio (the dominant computational overhead in GRPO) is unnecessary, and that the design should be reframed around trust region rather than IS correction. Directly relevant to the broader convergence/stability thread (GA-GRPO, BRAT, Controlling Sharpening) and complements the OMA paper (found same day) which also identifies implicit accounting problems in multi-turn GRPO.

## My Thoughts

<!-- Add your own notes here -->
