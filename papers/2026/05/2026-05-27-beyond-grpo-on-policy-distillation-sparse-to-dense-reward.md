---
title: "Beyond GRPO and On-Policy Distillation: An Empirical Sparse-to-Dense Reward Principle for Language-Model Post-Training"
authors: ["Yuanda Xu", "Hejian Sang", "Zhengze Zhou", "Ran He", "Zhipeng Wang", "Alborz Geramifard"]
date: 2026-05-27
arxiv_id: "2605.12483v4"
url: "http://arxiv.org/abs/2605.12483v4"
score: 0.87
topics: [GRPO, PPO, RL training, reward model, RLHF]
status: unread
---

# Beyond GRPO and On-Policy Distillation: An Empirical Sparse-to-Dense Reward Principle for Language-Model Post-Training

## Summary

This paper establishes a reward-density allocation principle: sparse sequence-level RL reward is best for strong teacher models that can explore, while dense token-level supervision is more efficient for compressing behaviors into smaller deployment models. A 4-stage workflow (teacher RL → forward-KL warmup → on-policy distillation → optional student RL) consistently outperforms direct GRPO at fixed deployment-student size, with RL-teacher vs raw-teacher transfer yielding +7.8 MATH and +5.4 AIME2024 points.

## Key Contributions

- Sparse-to-dense reward allocation principle: use scarce labeled data on teachers, dense transfer on students
- 4-stage workflow: teacher GRPO → forward-KL warmup → on-policy distillation → optional student RL
- Component ablation confirming each stage is load-bearing (no single stage is redundant)
- Replicates on Llama-3.1-8B + Llama-3.3-70B teacher, confirming generality

## Relevance

Directly bridges the token-level credit assignment theme (today's focus) with the sparse/dense reward tradeoff studied in SD-Zero (May 24). This paper provides the practical allocation rule that governs *when* to use dense token-level reward vs sparse outcome reward across the teacher-student training pipeline.

## My Thoughts

<!-- Add your own notes here -->
