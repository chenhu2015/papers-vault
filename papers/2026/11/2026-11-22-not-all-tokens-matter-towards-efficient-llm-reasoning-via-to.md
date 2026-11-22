---
title: "Not All Tokens Matter: Towards Efficient LLM Reasoning via Token Significance in Reinforcement Learning"
authors: ["Hanbing Liu", "Lang Cao", "Yuanyi Ren", "Mengyu Zhou", "Haoyu Dong", "Xiaojun Ma", "Shi Han", "Dongmei Zhang"]
date: 2025-06-09
arxiv_id: "2506.08125"
url: "https://arxiv.org/abs/2506.08125"
score: 0.76
topics: [RL training, GRPO, reward model, LLM]
status: unread
---

# Not All Tokens Matter: Towards Efficient LLM Reasoning via Token Significance in Reinforcement Learning

## Summary

This paper reframes RL length optimization through token significance: observing that many CoT tokens contribute negligibly to final answers, it proposes a significance-aware length reward that selectively penalizes only low-significance tokens, preserving essential reasoning steps. It further introduces a dynamic length reward that shifts from favoring detailed reasoning early in training to conciseness later, complementing the significance filter. Integrated into standard policy optimization, the approach achieves substantial response length reduction while preserving or improving accuracy across multiple reasoning benchmarks.

## Key Contributions

- Token significance analysis: many chain-of-thought tokens contribute negligibly to the final answer — standard uniform length penalties harm correctness by treating all tokens equally
- Significance-aware length reward: selectively penalizes only low-significance tokens while preserving essential reasoning steps
- Dynamic length reward: curriculum shift from detail-favoring early training to conciseness-favoring later training
- Integrates into standard policy optimization (compatible with GRPO-style training)

## Relevance

Orthogonal mechanism to DOT (Anti-Length Shift) for the same RLVR length efficiency problem: DOT targets response-length distribution outliers at the rollout level, while this paper targets token-level significance within responses. Both are more principled than naive length penalties. Part of the TON-adjacent adaptive reasoning efficiency cluster explored in today's digest.

## My Thoughts

<!-- Add your own notes here -->
