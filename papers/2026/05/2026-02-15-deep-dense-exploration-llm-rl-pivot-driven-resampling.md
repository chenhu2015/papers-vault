---
title: "Deep Dense Exploration for LLM Reinforcement Learning via Pivot-Driven Resampling"
authors: ["Yiran Guo", "Zhongjian Qiao", "Yingqi Xie", "Jie Liu", "Dan Ye", "Ruiqing Zhang", "Shuang Qiu", "Lijie Xu"]
date: 2026-02-15
arxiv_id: "2602.14169v1"
url: "http://arxiv.org/abs/2602.14169v1"
score: 0.80
topics: [RL training, GRPO, reward model]
status: unread
---

# Deep Dense Exploration for LLM Reinforcement Learning via Pivot-Driven Resampling

## Summary

DEEP-GRPO identifies 'pivot states' — deep, recoverable positions within failed trajectories that standard GRPO under-explores by only sampling from the root — and applies local dense resampling around them to discover correct suffixes. A dual-stream objective decouples global policy learning from local corrective updates, stabilising training. Outperforms GRPO and tree-based exploration baselines on mathematical reasoning benchmarks.

## Key Contributions

- Defines "pivot states" as deep, recoverable states in unsuccessful trajectories that standard GRPO misses
- Lightweight data-driven utility function to auto-balance recoverability and depth bias for pivot selection
- Local dense resampling at each pivot to increase probability of finding correct subsequent trajectories
- Dual-stream optimisation objective separating global learning from local corrective updates

## Relevance

Directly extends GRPO — a keyword and core topic in the interest profile — by addressing the under-exploration of error-prone deep states. Complements the step-level credit assignment angle (StePPO, ProceedRL) from yesterday by attacking the same multi-step failure problem from the exploration side rather than the credit side.

## My Thoughts

<!-- Add your own notes here -->
