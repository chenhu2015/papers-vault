---
title: "Precise: SDE-Consistent Stochastic Sampling for RL Post-Training of Flow-Matching Models"
authors: ["Jade Zou", "Tao Huang", "Weijie Kong", "Junzhe Li", "Yue Wu", "Qi Tian", "Jiangfeng Xiong", "Jianwei Zhang", "Liefeng Bo", "Zhao Zhong"]
date: 2026-05-25
arxiv_id: "2605.23522v1"
url: "http://arxiv.org/abs/2605.23522v1"
score: 0.79
topics: [RL training, multimodal models, reward model, reinforcement learning]
status: unread
---

# Precise: SDE-Consistent Stochastic Sampling for RL Post-Training of Flow-Matching Models

## Summary

Precise addresses the critical design problem of stochastic samplers for RL post-training of flow-matching image generation models, decomposing the challenge into exploration-stability balance and SDE discretization fidelity. The proposed sampler freezes the clean-latent posterior mean to keep denoising trajectories SDE-consistent, resolving excess discretization noise while enabling effective reward exploration. On image alignment benchmarks (PickScore, HPSv2.1), Precise achieves SOTA while requiring 13–53% less wall-clock training time than prior samplers.

## Key Contributions

- Identifies two interdependent components of stochastic sampler design: exploration-stability balance and SDE discretization fidelity
- Derives an SDE schedule that analytically balances exploration vs. denoising stability for RL training
- Novel "frozen posterior mean" approximation keeps the denoising trajectory SDE-consistent across small step counts
- 13–53% wall-clock training time reduction vs. best prior samplers, SOTA on PickScore and HPSv2.1

## Relevance

This is RL training methodology applied to multimodal generative models — an unexplored angle in this digest series. The interest profile includes multimodal models and RL training; Precise is directly about improving RL post-training efficiency for flow-matching image generators. Arrived from the new "RL for generative models" search angle introduced today.

## My Thoughts

<!-- Add your own notes here -->
