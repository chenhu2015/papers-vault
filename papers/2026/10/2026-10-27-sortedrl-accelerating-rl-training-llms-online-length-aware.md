---
title: "SortedRL: Accelerating RL Training for LLMs through Online Length-Aware Scheduling"
authors: ["Yiqi Zhang", "Huiqiang Jiang", "Xufang Luo", "Zhihe Yang", "Chengruidong Zhang", "Yifei Shen", "Dongsheng Li", "Yuqing Yang", "Lili Qiu", "Yang You"]
date: 2026-03-24
arxiv_id: "2603.23414"
url: "https://arxiv.org/abs/2603.23414"
score: 0.80
topics: [reinforcement learning, RL training, GRPO, agentic RL]
status: unread
---

# SortedRL: Accelerating RL Training for LLMs through Online Length-Aware Scheduling

## Summary

SortedRL addresses the rollout-phase bottleneck in LLM RL training — which can consume up to 70% of total training time for long-trajectory tasks — by reordering rollout samples by output length so that short samples form groups for early policy updates, enabling large rollout batches and near on-policy micro-curriculum construction simultaneously. A cache-based mechanism controls the degree of off-policy training, and a stateful controller manages rollout and update separately. Experiments on LLaMA-3.1-8B and Qwen-2.5-32B reduce bubble ratios by over 50% and yield 3.9–18.4% performance improvement over baseline with identical data.

## Key Contributions

- Length-aware rollout reordering: short samples grouped for early policy updates, reducing synchronisation overhead
- Enables large rollout batches + flexible update batches simultaneously — orthogonal to content-based selection methods
- Cache-based off-policy degree control to maintain near on-policy guarantees without full synchronisation
- Stateful RL controller with separate rollout buffer infrastructure — complements JigsawRL's pipeline multiplexing

## Relevance

Sits at the intersection of the RL rollout efficiency cluster and the RL systems / infrastructure thread (JigsawRL, LoongSage). Where JigsawRL addresses pipeline-level parallelism and LoongSage addresses async agentic RL, SortedRL addresses the within-rollout scheduling dimension — length-induced bubble ratios. Together with JigsawRL, this further populates the rollout infrastructure sub-thread.

## My Thoughts

<!-- Add your own notes here -->
