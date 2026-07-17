---
title: "Prune-OPD: Efficient and Reliable On-Policy Distillation for Long-Horizon Reasoning"
authors: ["Zhicheng Yang", "Zhijiang Guo", "Yifan Song", "Minrui Xu", "Yongxin Wang", "Yiwei Wang", "Xiaodan Liang", "Jing Tang"]
date: 2026-07-17
arxiv_id: "2605.07804v3"
url: "http://arxiv.org/abs/2605.07804v3"
score: 0.76
topics: [RL training, agentic RL, reinforcement learning]
status: unread
---

# Prune-OPD: Efficient and Reliable On-Policy Distillation for Long-Horizon Reasoning

## Summary

Addresses a critical flaw in OPD for long-horizon tasks: when the student's generated prefix diverges from the teacher's thought process, the teacher's dense reward signal becomes locally unexploitable, yet training continues to waste compute on these drifted trajectories. Prune-OPD monitors student-teacher top-k token overlap in real time, detects prefix-drift events, monotonically down-weights subsequent unreliable rewards, and triggers dynamic rollout truncation. Reduces training time 37-68% while preserving or improving performance on AMC, AIME, and HMMT; when student-teacher compatibility remains high, it automatically expands the training window instead.

## Key Contributions

- Identifies prefix-drift as the key failure mode of OPD on long-horizon tasks: divergent student prefix makes teacher dense reward locally unexploitable
- Real-time prefix-drift detection via student-teacher top-k token overlap monitoring
- Dynamic rollout truncation: monotonically down-weights rewards post-drift and halts generation; expands window when compatible
- 37-68% training time reduction while improving or matching performance on AMC, AIME, HMMT

## Relevance

Structurally parallel to TurnOPD (today) but at a different granularity: TurnOPD identifies wasted turns via probe statistics, Prune-OPD identifies wasted tokens within turns via top-k overlap. Together they diagnose the same problem — compute waste in long-horizon OPD — from complementary angles. The prefix-drift mechanism is also the OPD analog of ARMOR's off-policy drift problem: in both cases, distribution divergence between the reference policy and the training trajectory degrades the supervision signal.

## My Thoughts

<!-- Add your own notes here -->
