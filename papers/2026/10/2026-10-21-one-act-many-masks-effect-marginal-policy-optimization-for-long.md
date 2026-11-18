---
title: "One Act, Many Masks: Effect-Marginal Policy Optimization for Long-Horizon Agents"
authors: ["Shaojin Ma", "Ruitao Wang", "Pengyi Li", "Jie Yang", "Liangyu Chen", "Gangyi Zhao", "Hongyao Tang", "Yan Zheng", "Jianye Hao"]
date: 2026-10-21
arxiv_id: "2610.29427v1"
url: "http://arxiv.org/abs/2610.29427v1"
score: 0.85
topics: [agentic RL, RL training, LLM agent]
status: unread
---

# One Act, Many Masks: Effect-Marginal Policy Optimization for Long-Horizon Agents

## Summary

Identifies credit-update misalignment in multi-turn RL for LLM agents: different textual responses inducing the same executable effect receive credit tied to their individual textual realizations, misaligning policy update directions from true execution-level outcomes. Proposes Effect-Marginal Policy Optimization (EMPO), which couples policy updates across alternative textual realizations via an effect-level surrogate that preserves the original credit signals. No additional critics or rollouts required; outperforms strong baselines on ALFWorld, WebShop, and Sokoban.

## Key Contributions

- Identifies "credit-update misalignment" as a structural problem in multi-turn LLM agent RL: response-specific probability ratios assign credit based on textual identity rather than executable equivalence
- EMPO: an effect-level surrogate that couples policy updates across alternative textual realizations of the same executable action
- Compatible with both trajectory-level and step-level credit estimators; zero overhead (no additional critics or rollouts)
- Demonstrated gains in both task performance and learning efficiency on ALFWorld, WebShop, and Sokoban

## Relevance

Directly extends the multi-turn OPSD cluster (Skill-SD, ActFirst-OPD, MVPO, SAGE-OPD) by addressing a different layer of the multi-turn RL problem: not how to assign credit across turns, but how to align policy updates with execution-level equivalence within a turn. The "effect-marginal" framing is a genuinely new mechanism orthogonal to all existing multi-turn OPSD entries.

## My Thoughts

<!-- Add your own notes here -->
