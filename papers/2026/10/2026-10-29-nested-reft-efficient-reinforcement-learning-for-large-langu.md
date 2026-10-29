---
title: "Nested-ReFT: Efficient Reinforcement Learning for Large Language Model Fine-Tuning via Off-Policy Rollouts"
authors: ["Maxime Heuillet", "Yufei Cui", "Boxing Chen", "Audrey Durand", "Prasanna Parthasarathi"]
date: 2026-10-29
arxiv_id: "2508.10123v3"
url: "http://arxiv.org/abs/2508.10123v3"
score: 0.82
topics: [RL training, agentic RL, reinforcement learning]
status: unread
---

# Nested-ReFT: Efficient Reinforcement Learning for Large Language Model Fine-Tuning via Off-Policy Rollouts

## Summary

Nested-ReFT reduces LLM RL post-training inference cost by repurposing a layer-skipping subset of the target model as an off-policy behavior model to generate rollout completions. Theoretical analysis shows the approach yields unbiased gradient estimates with controlled variance despite the off-policy divergence. Empirical results show improved tokens/sec across math reasoning benchmarks while matching baseline ReFT accuracy via three bias-mitigation variants.

## Key Contributions

- Layer-skipping behavior model: a dynamic subset of target model layers acts as the off-policy rollout generator, reducing inference cost without a separate smaller model
- Theoretical guarantee: unbiased gradient estimates with controlled variance despite off-policy rollout distribution
- Three bias-mitigation variants to manage off-policyness in gradient updates
- Improved tokens/sec efficiency across multiple math reasoning benchmarks and model sizes

## Relevance

Directly extends the RL rollout efficiency cluster (now 12 entries) with a novel architecture-level approach: instead of selecting or filtering rollouts (I-PPO, LEEPS, TrajVal), it cheapens rollout generation itself via layer-skip off-policy sampling. Complements content-based selection papers already in the cluster with an inference-cost reduction angle.

## My Thoughts

<!-- Add your own notes here -->
