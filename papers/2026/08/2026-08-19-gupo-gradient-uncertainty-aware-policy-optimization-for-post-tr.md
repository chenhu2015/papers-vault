---
title: "GUPO: Gradient Uncertainty-aware Policy Optimization for Post-Training Large Language Models"
authors: ["Peizheng Guo", "Jianqi Zhang", "Xingyu Zhang", "Yun Fan"]
date: 2026-08-18
arxiv_id: "2608.17411v1"
url: "https://arxiv.org/abs/2608.17411"
score: 0.88
topics: [GRPO, RL training, RLAIF]
status: unread
---

# GUPO: Gradient Uncertainty-aware Policy Optimization for Post-Training Large Language Models

## Summary

GUPO identifies that group-gradient conflicts in GRPO's mini-batch aggregation are associated with less effective policy updates. It models each group gradient as a random variable under a Bayesian-Dirichlet formulation, estimating gradient uncertainty to calibrate each gradient's contribution during aggregation rather than averaging them uniformly. Experiments across multiple benchmarks demonstrate consistent improvement over standard GRPO.

## Key Contributions

- Empirical analysis showing group-gradient conflicts in GRPO correlate with less effective policy updates
- Bayesian formulation modelling each group gradient as a random variable with an estimated probability distribution
- Dirichlet-based gradient uncertainty estimation used to calibrate per-group-gradient contribution weight during aggregation
- Benchmark experiments demonstrating GUPO outperforms standard GRPO across multiple reasoning tasks

## Relevance

GRPO is a core keyword in the interest profile; this paper addresses a fundamental flaw in GRPO's gradient aggregation step that has been overlooked in the process reward and training-efficiency literature accumulated since May. The Bayesian-Dirichlet framing is a novel angle that complements the variance-reduction approaches (SRGPO, Temporal GRPO) already in the vault.

## My Thoughts

<!-- Add your own notes here -->
