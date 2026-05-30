---
title: "RUBRIC-ARROW: Alternating Pointwise Rubric Reward Modeling for LLM Post-training in Non-verifiable Domains"
authors: ["Haoxiang Jiang", "Zihan Dong", "Tianci Liu", "Wanying Wang", "Ran Xu", "Tony Yu", "Linjun Zhang", "Haoyu Wang"]
date: 2026-05-27
arxiv_id: "2605.29156"
url: "http://arxiv.org/abs/2605.29156v1"
score: 0.79
topics: [reward model, GRPO, RLHF, RL training]
status: unread
---

# RUBRIC-ARROW: Alternating Pointwise Rubric Reward Modeling for LLM Post-training in Non-verifiable Domains

## Summary

RUBRIC-ARROW jointly trains a rubric generator and a rubric-conditioned judge in alternating GRPO phases, using a probability-based scoring rule to reduce ties (a key failure mode of Boolean rubric aggregation) and phase-specific preference-based rewards. Extensive experiments show competitive reward-modeling accuracy and consistent gains for downstream policy post-training on non-verifiable open-ended tasks.

## Key Contributions

- Alternating training of rubric generator + rubric-conditioned judge with GRPO
- Probability-based scoring rule reduces ties vs. hard Boolean aggregation
- Phase-specific preference-based rewards for each alternating phase
- Competitive reward-modeling accuracy without requiring frontier LLMs for rubric generation

## Relevance

Addresses rubric-based reward modeling for non-verifiable domains — complementary to RLR³ (verifiable) and Soft-SVeRL (partial verification) found today; fills a gap in the reward design landscape for open-ended tasks.

## My Thoughts

<!-- Add your own notes here -->
