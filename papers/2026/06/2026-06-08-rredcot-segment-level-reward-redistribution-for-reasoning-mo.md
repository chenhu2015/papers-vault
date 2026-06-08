---
title: "RREDCoT: Segment-Level Reward Redistribution for Reasoning Models"
authors: ["Mykyta Ielanskyi", "Kajetan Schweighofer", "Lukas Aichberger", "Sepp Hochreiter"]
date: 2026-06-04
arxiv_id: "2606.06475v1"
url: "http://arxiv.org/abs/2606.06475v1"
score: 0.78
topics: [GRPO, reward model, RL training, reinforcement learning, PPO]
status: unread
---

# RREDCoT: Segment-Level Reward Redistribution for Reasoning Models

## Summary

RREDCoT addresses the high-variance problem in GRPO/Monte Carlo credit assignment for CoT reasoning by using the model itself to approximate optimal reward redistribution without additional generation passes. It segments CoT traces and estimates intermediate state values, emphasizing steps important for reaching the correct solution while avoiding the compute overhead of MC sampling. The work also systematically investigates CoT segmentation granularity and state value estimation strategies.

## Key Contributions

- Framing of GRPO/CoT training as a delayed reward problem where MC methods suffer from high variance
- Self-approximated reward redistribution: uses the model's own representations to estimate optimal redistribution without extra generation
- Investigation of CoT segmentation strategies and state value estimation methods
- Comparison against MC sampling and attribution-based baselines showing efficiency and quality gains

## Relevance

Fills a gap in the GRPO credit assignment thread (EP-GRPO/M-GRPO from June 2, RREDCoT). Where June 2's EP-GRPO used entropy-gated process supervision and M-GRPO used momentum anchoring for stability, RREDCoT specifically attacks the variance problem in delayed-reward CoT training via redistribution — a complementary angle.

## My Thoughts

<!-- Add your own notes here -->
