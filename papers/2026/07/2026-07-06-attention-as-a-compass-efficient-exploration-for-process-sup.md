---
title: "Attention as a Compass: Efficient Exploration for Process-Supervised RL in Reasoning Models"
authors: []
date: 2025-09-30
arxiv_id: "2509.26628v1"
url: "http://arxiv.org/abs/2509.26628v1"
score: 0.71
topics: [RL training, RLHF, GRPO, reward model, reinforcement learning]
status: unread
---

# Attention as a Compass: Efficient Exploration for Process-Supervised RL in Reasoning Models

## Summary

This paper introduces attention-pattern guidance as an exploration compass for process-supervised RL (PSRL) in LLM reasoning, using attention signals to identify efficient branching positions in the reasoning tree and improve sampling strategy, addressing limited exploration efficiency in existing PSRL approaches. It connects the process supervision thread (PASS middleware framework) with the exploration failure mode thread (AREW/SeL/TA-GRPO), proposing that the model's own attention structure can serve as a cheap, intrinsic signal for where dense process supervision and rollout branching are most needed.

## Key Contributions

- Diagnosis of limited exploration efficiency in PSRL — both in terms of where to branch (branching positions) and how to sample (sampling strategy)
- Attention-based compass: using the model's own attention patterns to identify high-leverage branching points in the reasoning tree, reducing the cost of dense PSRL supervision
- Improved exploration efficiency relative to existing PSRL baselines on reasoning benchmarks
- Intrinsic signal approach — no external model or annotation required for guiding branching decisions

## Relevance

Fills a gap between the process supervision thread (PASS's step-level middleware, ReasonRAG's role-typed rewards) and the exploration failure thread (SeL, TA-GRPO, RL-PLUS) by showing that the model's own attention structure can bridge both: it both identifies where process rewards are most informative and determines where rollout branching will yield the highest exploration value. This is the PSRL-specific analog of BiPACE's (Jul 3) insight that the policy's own hidden-state geometry should define the state-partition for advantage estimation.

## My Thoughts

<!-- Add your own notes here -->
