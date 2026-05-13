---
title: "VCRL: Variance-based Curriculum Reinforcement Learning for Large Language Models"
authors: ["Guochao Jiang", "Wenfeng Feng", "Guofeng Quan", "Chuzhan Hao", "Yuewei Zhang", "Guohua Liu", "Hao Wang"]
date: 2025-09-24
arxiv_id: "2509.19803v1"
url: "http://arxiv.org/abs/2509.19803v1"
score: 0.82
topics: [RL training, GRPO, reinforcement learning, reward model]
status: unread
---

# VCRL: Variance-based Curriculum Reinforcement Learning for Large Language Models

## Summary

VCRL uses the variance of GRPO rollout group rewards as an online difficulty signal: low-variance training batches — where the model either consistently succeeds or consistently fails — contribute minimal learning signal and are deprioritized, while high-variance batches representing the learning frontier are prioritized. This variance-based curriculum requires no external difficulty estimator and outperforms GRPO, DAPO, and GSPO baselines across five mathematical reasoning benchmarks on two models.

## Key Contributions

- Identifies reward-variance within a GRPO rollout group as a proxy for sample difficulty without needing annotations
- Low variance → too easy (all correct, no contrastive signal) or too hard (all wrong, no positive signal)
- High variance → optimal difficulty range where the model can still learn from contrastive rollouts
- Dynamically schedules training batches based on this variance signal with no auxiliary model
- Consistent improvements over GRPO/DAPO/GSPO on MATH, AMC, AIME, and similar benchmarks

## Relevance

Directly connects to the GRPO and reward model core interests, offering a principled explanation for why group reward variance is the natural curriculum signal in rollout-based RLVR. The insight pairs well with METIS (also in today's digest) which internalizes this same variance signal — together they form a complete picture of variance-based curriculum RL for LLMs.

## My Thoughts

<!-- Add your own notes here -->
