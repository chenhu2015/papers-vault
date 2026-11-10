---
title: "TGRL: Temperature-Grouped Reinforcement Learning for Efficient Exploration in LLMs"
authors: ["Zihan Lin", "Xiaohan Wang", "Jie Cao", "Jiajun Chai", "Wei Lin", "Guojun Yin", "Ran He"]
date: 2026-09-27
arxiv_id: "2609.33589v1"
url: "https://arxiv.org/abs/2609.33589"
score: 0.80
topics: [GRPO, RLVR, agentic RL, reward model, RL training]
status: unread
---

# TGRL: Temperature-Grouped Reinforcement Learning for Efficient Exploration in LLMs

## Summary

TGRL partitions each prompt's rollout group into low- and high-temperature subsets, uses the reward contrast between them as an exploration-gain estimate, and allocates this group-level signal as token-level credit via Jensen-Shannon divergence between the temperature-scaled next-token distributions. This converts temperature-induced diversity into an explicit training signal without expanding the rollout budget, achieving 36% faster convergence and broad gains across math (+1.6% at 32B), code (+196.7 CodeForces), and agentic (+6.3%/4.9% ALFWorld/WebShop) benchmarks.

## Key Contributions

- Temperature-grouped partition: splits each prompt's rollout into low-T / high-T subsets; reward contrast estimates per-group exploration gain
- JS divergence credit allocation: token-level credit derived from JS divergence between temperature-scaled next-token distributions of the same logits
- No rollout budget expansion: exploration signal is free — extracted from the same rollout sample budget as standard GRPO
- Broad multi-domain gains: 36% faster convergence; +1.6% math avg at 32B, +196.7 CodeForces, +4.4% LiveCodeBench Pass@16, +6.3%/4.9% ALFWorld/WebShop

## Relevance

TGRL is directly relevant to the GRPO training dynamics thread (Reward Budgeting, Controlling Sharpening, VeXact) and the RL rollout efficiency thread. The JS divergence credit mechanism is a new tool for exploration-aware advantage estimation that addresses entropy collapse without algorithmic regularization, complementing the weak-model prefix guidance angle (Boosting via Weak-Model paper same search).

## My Thoughts

<!-- Add your own notes here -->
