---
title: "Adapt to Thrive! Adaptive Power-Mean Policy Optimization for Improved LLM Reasoning"
authors: ["Yiming Huang", "Zhenbo Shi", "Shuzheng Gao", "Cuiyun Gao", "Peiyi Han"]
date: 2026-04-11
arxiv_id: "2605.04066"
url: "https://arxiv.org/abs/2605.04066"
score: 0.78
topics: [RLVR, GRPO, PPO, reinforcement learning, RL training]
status: unread
---

# Adapt to Thrive! Adaptive Power-Mean Policy Optimization for Improved LLM Reasoning

## Summary

APMPO proposes an adaptive policy optimization objective for RLVR where the aggregation function dynamically transitions from arithmetic-mean behavior (signal amplification for weaker models) to geometric-mean behavior (consistency enforcement for stronger models) via a generalized power-mean objective. Feedback-Adaptive Clipping adjusts PPO clipping bounds dynamically based on real-time reward statistics, avoiding the limitations of static clipping. APMPO improves average Pass@1 on mathematical reasoning by 3.0 points over GRPO across nine benchmarks.

## Key Contributions

- Power-Mean Policy Optimization (PMPO): generalized power-mean aggregation that interpolates between arithmetic (p=1) and geometric (p→0) mean, allowing adaptive behavior across training stages
- Feedback-Adaptive Clipping (FAC): adjusts epsilon clipping bounds based on real-time reward statistics rather than a fixed constant
- +3.0 pp average Pass@1 on math reasoning vs GRPO across 9 benchmarks using Qwen2.5-3B-Instruct
- Addresses the mismatch between static policy optimization assumptions and the model's evolving capability during RL training

## Relevance

APMPO extends the GRPO/RLVR training methodology cluster, introducing an adaptive aggregation objective that is orthogonal to other GRPO variants (MinPRO, EPIC, LGPO focused on importance ratio; HATCH/Failure-Prefix focused on data difficulty; DASD/HSD focused on teacher direction). The power-mean approach is a novel parameterization of the GRPO objective that hasn't appeared in earlier digests.

## My Thoughts

<!-- Add your own notes here -->
