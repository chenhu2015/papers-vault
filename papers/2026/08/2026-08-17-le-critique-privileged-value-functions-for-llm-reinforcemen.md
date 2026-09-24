---
title: "Le Critique: Privileged Value Functions for LLM Reinforcement Learning"
authors: ["Siddarth Venkatraman", "Matthieu Dinot", "Laurence Aitchison"]
date: 2026-08-17
arxiv_id: "2608.16739v1"
url: "https://arxiv.org/abs/2608.16739"
score: 0.82
topics: [GRPO, RL training, reward model, PPO]
status: unread
---

# Le Critique: Privileged Value Functions for LLM Reinforcement Learning

## Summary

Proposes Privileged Value Functions (PVF) that inject task-relevant token-level supervision into LLM RL without biasing the policy gradient, and TETHER, a baseline that adaptively interpolates between group-relative (GRPO-style) and learned value baselines depending on value function accuracy. Both consistently outperform the standard value-function baseline across reasoning tasks and are competitive with or better than mean-baseline GRPO, without the straggler-blocking and off-policy issues of large rollout groups.

## Key Contributions

- Privileged Value Functions (PVF): provides token-level advantage signal by injecting task-relevant information that is available during training but not at inference; no policy bias
- TETHER: adaptive interpolation between group-relative and value baselines; uses value function accuracy to gate which baseline is active
- Identifies two GRPO pathologies addressed: (1) sequence-level credit only, (2) straggler rollouts block training and increase off-policyness
- Competitive with or better than mean-baseline GRPO on reasoning tasks; consistently better than standard value-function baseline

## Relevance

Directly relevant to the GRPO improvement thread — fills a gap between critic-free GRPO and full critic-based PPO. PVF's token-level credit without policy bias is architecturally adjacent to the ECHO credit routing problem (which addressed intra-trajectory credit attribution). TETHER's adaptive baseline could combine with GVPO's importance-sampling-free formulation for a more stable hybrid.

## My Thoughts

<!-- Add your own notes here -->
