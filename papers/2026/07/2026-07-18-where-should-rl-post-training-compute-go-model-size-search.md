---
title: "Where Should RL Post-Training Compute Go? Model Size, Search, Learning, and Feedback"
authors: ["Patrick Wilhelm", "Odej Kao"]
date: 2026-07-15
arxiv_id: "2607.13389"
url: "https://arxiv.org/abs/2607.13389"
score: 0.80
topics: [GRPO, RL training, reward model, reinforcement learning, PPO]
status: unread
---

# Where Should RL Post-Training Compute Go? Model Size, Search, Learning, and Feedback

## Summary

Introduces a FLOP-accounting framework for GRPO post-training that decomposes compute into rollout/search, policy-update/learning, and reward-model evaluation components. Finds conditional allocation frontiers that vary with model size, compute budget, reward system, and evaluation target — larger policies buy fewer updates/rollouts per FLOP budget, so model choice and training allocation are inherently coupled. Rule-based rewards spend nearly all non-update compute on rollouts while PRM-style feedback allocates substantial budget to reward-model inference, with a diagnostic protocol (RACE) for identifying allocation regimes before expensive full training runs.

## Key Contributions

- FLOP-accounting framework for GRPO post-training: decomposes budget into rollout/search, policy-update/learning, and reward/feedback-model evaluation
- Conditional allocation frontiers: optimal compute split changes with model size, budget magnitude, reward system type, and evaluation task
- Coupling insight: larger policies consume more per-token compute and therefore buy fewer updates or rollouts under same budget — model choice and training allocation cannot be decided independently
- Reward system changes accounting: rule-based rewards concentrate compute on rollouts; PRM-style feedback requires significant reward-model inference budget; introduces RACE diagnostic pilot protocol

## Relevance

Practical complement to the vault's RL optimization internals thread (RIPO, EGRSD, Prune-OPD, TurnOPD, Value-Gradient Hypothesis). While those papers improve algorithmic efficiency within a fixed compute scheme, this paper asks the higher-level allocation question: given a fixed FLOP budget, what is the best allocation across search/learning/reward? The PRM-vs-rule-based accounting insight also directly quantifies the cost of the PRM thread (GroundedPRM, KV-PRM, SCI-PRM) — PRM training budget must be counted against rollout opportunity cost.

## My Thoughts

<!-- Add your own notes here -->
