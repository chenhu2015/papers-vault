---
title: "Scaling Behaviors of LLM Reinforcement Learning Post-Training: An Empirical Study in Mathematical Reasoning"
authors: ["Zelin Tan", "Hejia Geng", "Xiaohang Yu", "Mulei Zhang", "Guancheng Wan", "Yifan Zhou", "Qiang He", "Xiangyuan Xue", "Heng Zhou", "Yutao Fan", "Zhongzhi Li", "Zaibin Zhang", "Guibin Zhang", "Chen Zhang", "Zhenfei Yin", "Philip Torr", "Lei Bai"]
date: 2025-09-29
arxiv_id: "2509.25300v4"
url: "http://arxiv.org/abs/2509.25300v4"
score: 0.84
topics: [RL training, GRPO, reinforcement learning, LLM agent]
status: unread
---

# Scaling Behaviors of LLM Reinforcement Learning Post-Training: An Empirical Study in Mathematical Reasoning

## Summary

Systematic empirical study of RL post-training scaling laws across the full Qwen2.5 series (0.5B–72B), modeling test loss, compute, and data with predictive power-laws that hold for both base and instruction-tuned models. Larger models have superior learning efficiency but show latent saturation trends in k(N); in data-constrained regimes, repeated high-quality data reuse is highly effective with performance governed by total optimization steps, not sample uniqueness. Provides principled guidelines for compute-efficient LLM RL post-training.

## Key Contributions

- Derives a predictive power-law for RL post-training that models test loss as a function of compute and data, robust across the full Qwen2.5 family
- Identifies latent saturation in learning efficiency k(N) as model size increases, suggesting diminishing returns at scale in RL post-training efficiency
- Shows repeated reuse of high-quality data outperforms diverse low-quality data in constrained regimes; performance tracks total optimization steps
- Complements "How RL Reshapes LLM Reasoning" (which focuses on strategy redistribution) with a resource-level compute/data scaling view

## Relevance

Core contribution to the RL training dynamics/scaling thread alongside "How RL Reshapes LLM Reasoning" (2610.04158v1) and Ring-Zero (2607.12395v2); provides the empirical power-law foundation across model scales that those papers describe theoretically and at extreme scales respectively.

## My Thoughts

<!-- Add your own notes here -->
