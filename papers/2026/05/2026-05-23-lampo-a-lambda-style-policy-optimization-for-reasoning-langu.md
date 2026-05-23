---
title: "LamPO: A Lambda Style Policy Optimization for Reasoning Language Models"
authors: ["Zhe Yuan", "Yipeng Zhou", "Jinghan Li", "Xinyuan Chen", "Bowen Deng", "Zhiqian Chen", "Liang Zhao"]
date: 2026-05-23
arxiv_id: "2605.21235v1"
url: "http://arxiv.org/abs/2605.21235v1"
score: 0.80
topics: [GRPO, RLHF, PPO, RL training, reinforcement learning, reward model]
status: unread
---

# LamPO: A Lambda Style Policy Optimization for Reasoning Language Models

## Summary

LamPO replaces GRPO's scalar group-mean baseline with a Pairwise Decomposed Advantage that aggregates reward differentials across all response pairs in a rollout group, modulated by confidence-aware log-probability weights. This preserves the full relational topology of sampled trajectories rather than collapsing it to a single number, sharpening credit assignment under sparse outcome rewards. Experiments on AIME24/25, MATH-500, and GPQA-Diamond with Qwen3 and Phi-4 backbones show consistent improvement over GRPO and recent RLVR variants with more stable training dynamics.

## Key Contributions

- Pairwise Decomposed Advantage: reformulates GRPO advantage as integrated pairwise reward gaps within a rollout group, weighted by confidence derived from log-probability differences
- Provably finer credit signal than scalar group-mean baselines in rank-sensitive reward landscapes
- Optional ROUGE-L dense auxiliary reward to reduce outcome sparsity when reference solutions are available
- Consistent improvements on AIME24, AIME25, MATH-500, GPQA-Diamond across Qwen3-1.7B, Qwen3-4B, Phi-4-mini

## Relevance

Directly advances the GRPO/RLVR optimization thread that has been the backbone of this digest series. Complements May 22's DelTA (token-level credit from discriminative analysis) and May 20's CEPO (contrastive token credit) by attacking the group-level aggregation problem rather than the token-level one.

## My Thoughts

<!-- Add your own notes here -->
