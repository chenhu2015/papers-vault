---
title: "Efficient RL Training for LLMs with Experience Replay"
authors: ["Charles Arnal", "Vivien Cabannes", "Taco Cohen", "Julia Kempe", "Remi Munos"]
date: 2026-10-25
arxiv_id: "2604.08706v1"
url: "http://arxiv.org/abs/2604.08706v1"
score: 0.82
topics: [RL training, RLHF, GRPO, reinforcement learning]
status: unread
---

# Efficient RL Training for LLMs with Experience Replay

## Summary

This work challenges the assumption that strict on-policy data is essential for LLM RL post-training, formalizing the optimal replay buffer design as a trade-off between staleness-induced variance, sample diversity, and generation cost. Empirically, a well-designed replay buffer drastically reduces inference compute without degrading — and sometimes improving — final model performance and policy entropy. The result directly challenges the prevailing on-policy dogma in LLM RL.

## Key Contributions

- Formal framework: replay buffer design as staleness-induced variance vs. sample diversity vs. generation cost tradeoff
- Shows strict on-policy sampling is suboptimal when generation is expensive — a principled argument, not just an empirical observation
- Replay buffer preserves or improves model performance and policy entropy while drastically reducing inference compute
- Systematic study across model configurations with controlled ablations

## Relevance

Directly relevant to the RL training dynamics/scaling thread (Oct 23–24): while IsoCompute, VIGOR, and Scaling Behaviors focus on how to allocate rollouts efficiently, Experience Replay asks the more radical question of whether fresh rollouts are necessary at all. If confirmed, this reframes the entire compute budget discussion — the ceiling is lower than assumed.

## My Thoughts

<!-- Add your own notes here -->
