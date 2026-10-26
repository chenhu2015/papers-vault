---
title: "Train at Moving Edge: Online-Verified Prompt Selection for Efficient RL Training of Large Reasoning Models"
authors: ["Jiahao Wu", "Ning Lu", "Shengcai Liu", "Kun Wang", "Yanting Yang", "Baijiong Lin", "Chen Jason Zhang", "Li Qing", "Ke Tang"]
date: 2026-03-26
arxiv_id: "2603.25184v3"
url: "http://arxiv.org/abs/2603.25184v3"
score: 0.85
topics: [RLHF, GRPO, RL training, reinforcement learning]
status: unread
---

# Train at Moving Edge: Online-Verified Prompt Selection for Efficient RL Training of Large Reasoning Models

## Summary

HIVE (History-Informed and online-VErified prompt selection) identifies that sample utility is non-uniform and evolves during training, concentrating at the 'learning edge' — the intersection of intermediate difficulty and high uncertainty — which shifts as training proceeds. It employs a dual-stage framework: historical reward trajectories for coarse selection plus prompt entropy as a real-time proxy to prune stale-utility instances before rollout. HIVE delivers significant rollout efficiency improvements across multiple math reasoning benchmarks without performance degradation.

## Key Contributions

- "Learning edge" concept: utility concentrates at the intersection of intermediate difficulty and high uncertainty, and this edge migrates during training
- Dual-stage selection: historical reward trajectory (coarse) + current prompt entropy (fine-grained real-time proxy)
- Demonstrates that large fractions of rollouts contribute negligible gradients and can be safely pruned
- Complementary to VIGOR (variance-guided rollout allocation) and LEEPS (explore-exploit prompt portfolio)

## Relevance

HIVE directly extends the RL rollout efficiency cluster (VIGOR, LEEPS, Experience Replay, JigsawRL, LLMZero) with a history-aware prompt selection method. The "learning edge" framing is distinct from VIGOR's variance signal and LEEPS's explore-exploit portfolio — it captures temporal evolution of utility, not just cross-prompt heterogeneity.

## My Thoughts

<!-- Add your own notes here -->
