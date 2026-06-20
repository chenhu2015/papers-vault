---
title: "SPS: Steering Probability Squeezing for Better Exploration in Reinforcement Learning for Large Language Models"
authors: ["Yifu Huo", "Chenglong Wang", "Ziming Zhu", "Shunjie Xing", "Peinan Feng", "Tongran Liu", "Qiaozhi He", "Tianhua Zhou", "Xiaojia Chang", "Jingbo Zhu", "Zhenghui Yu", "Tong Xiao"]
date: 2026-04-18
arxiv_id: "2604.16995v1"
url: "http://arxiv.org/abs/2604.16995v1"
score: 0.77
topics: [reinforcement learning, RL training, GRPO]
status: unread
---

# SPS: Steering Probability Squeezing for Better Exploration in Reinforcement Learning for Large Language Models

## Summary

SPS identifies a "squeezing effect" in RL for LLMs where probability mass concentrates excessively on a narrow set of high-reward trajectories, restricting exploration and capping Pass@k. SPS addresses this by interleaving standard RL with inverse RL (treating on-policy rollouts as demonstrations) to explicitly reshape the trajectory distribution without external supervision, improving Pass@k while maintaining Pass@1. Experiments on five reasoning benchmarks also yield an empirical upper bound on Pass@k as a diagnostic for intrinsic exploration limits.

## Key Contributions

- Formal analysis of the "squeezing effect": probability mass over-concentration on high-reward trajectories
- Inverse RL as a distribution-reshaping complement to forward RL (no external supervision required)
- Unified RL+IRL training loop with alternating phases
- Empirical Pass@k upper bound as a practical diagnostic for exploration saturation

## Relevance

SPS addresses the exploration failure mode identified as an emerging gap in the vault: it is the trajectory-distribution complement to existing exploration approaches. Where DiScO (Jun 9) maintained diversity at the policy-gradient direction level, ANCORA (Jun 15) grew the problem distribution via UCB curriculum, and S2L-PO (Jun 16) sourced diverse rollouts from smaller models, SPS explicitly reshapes the trajectory distribution itself using the RL rollouts as IRL demonstrations — a fourth, orthogonal exploration mechanism. The "squeezing effect" also provides a mechanistic explanation for why the GRPO zero-gradient problem (ARBOR, Jun 19) and outcome-homogeneous groups arise: successful trajectories crowd out the distribution, leaving no learning signal for the remaining prompts.

## My Thoughts

<!-- Add your own notes here -->
