---
title: "Beyond Uniform Token-Level Trust Region in LLM Reinforcement Learning"
authors: ["Renjie Mao", "Xiangxin Zhou", "Lvfang Tao", "Yixin Ding", "Yu Shi", "Yongguang Lin", "Yuheng Wu", "Honglin Zhu", "Qian Qiu", "Wenxi Zhu"]
date: 2026-06-09
arxiv_id: "2606.10968v1"
url: "http://arxiv.org/abs/2606.10968v1"
score: 0.82
topics: [reinforcement learning, RL training, PPO, GRPO, agentic RL]
status: unread
---

# Beyond Uniform Token-Level Trust Region in LLM Reinforcement Learning

## Summary

CPPO (Cumulative Prefix-divergence Policy Optimization) replaces PPO's position-agnostic token-level clipping with a dual mechanism: a position-weighted threshold that imposes stricter limits at early autoregressive positions (whose errors compound downstream) and a cumulative prefix budget that tracks how far the conditioning history has already deviated from the rollout policy. Together these mechanisms prevent early-stage drift while relaxing late-stage constraints, improving both training stability and reasoning accuracy across model scales.

## Key Contributions

- Formal diagnosis of two failure modes in uniform token-level trust regions: ignoring autoregressive asymmetry and evaluating divergence without prefix context
- Position-weighted threshold: stricter at early positions, relaxed at late positions, derived from a finite-horizon policy-improvement bound
- Cumulative prefix budget: dynamically restricts further deviation once prefix has already diverged significantly
- Empirical improvements in training stability and reasoning accuracy across various model scales

## Relevance

Directly advances the RL training thread — specifically the line running from PPO through GRPO/GSPO/CTPO on importance-sampling and trust-region design for LLM post-training. CPPO's position-weighted clipping is conceptually adjacent to CTPO's cumulative IS ratio (Jun 10 runner-up) and ConSteer-RL's confidence-aware shaping (Jun 9), but attacks the problem from the trust-region geometry side rather than the IS correction side.

## My Thoughts

<!-- Add your own notes here -->
