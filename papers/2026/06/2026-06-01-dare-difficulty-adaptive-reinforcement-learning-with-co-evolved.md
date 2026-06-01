---
title: "DARE: Difficulty-Adaptive Reinforcement Learning with Co-Evolved Difficulty Estimation"
authors: ["Yang Zhou", "Can Jin", "Zihan Dong", "Zhepeng Wang", "Yanting Yang", "Shiyu Zhao", "Lei Li", "Runxue Bao", "Yaochen Xie", "Dimitris N. Metaxas"]
date: 2026-06-01
arxiv_id: "2605.09188"
url: "https://arxiv.org/abs/2605.09188"
score: 0.79
topics: [GRPO, reinforcement learning, LLM agent]
status: unread
---

# DARE: Difficulty-Adaptive Reinforcement Learning with Co-Evolved Difficulty Estimation

## Summary

DARE co-evolves difficulty estimation with the policy via self-normalized importance sampling, preventing staleness under policy drift — a failure mode of static difficulty selection. A symmetric Beta sampling distribution maintains diverse difficulty coverage, while tailored training strategies per difficulty tier allocate compute adaptively, improving correctness on hard tasks and conciseness on easy ones simultaneously. Consistent improvements across multiple models and domains in both training efficiency and final performance.

## Key Contributions

- Identifies three limitations of existing difficulty-aware RL: stale estimates under policy drift, limited final-performance gains from selection alone, unchanged inference efficiency
- Self-normalized importance sampling to co-evolve difficulty estimates alongside the policy
- Symmetric Beta distribution for coverage across the difficulty spectrum
- Adaptive compute allocation: more compute on hard tasks, shorter responses on easy ones — simultaneously improving correctness and inference efficiency

## Relevance

Previous curriculum RL work in the digest (May 24 reasoning budget papers) focused on compute budgeting; DARE's angle of co-evolution to prevent difficulty estimate staleness is distinct and addresses a subtle but important failure mode in GRPO training data selection.

## My Thoughts

<!-- Add your own notes here -->
