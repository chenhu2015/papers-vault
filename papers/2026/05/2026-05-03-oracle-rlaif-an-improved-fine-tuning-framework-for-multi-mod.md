---
title: "Oracle-RLAIF: An Improved Fine-Tuning Framework for Multi-modal Video Models through Reinforcement Learning from Ranking Feedback"
authors: ["Derek Shi", "Ruben Glatt", "Christine Klymko", "Shubham Mohole", "Hongjun Choi", "Shashank Kushwaha", "Sam Sakla", "Felipe Leno da Silva"]
date: 2026-05-03
arxiv_id: "2510.02561v1"
url: "http://arxiv.org/abs/2510.02561v1"
score: 0.80
topics: [RLAIF, GRPO, multimodal, vision-language, reward model, VLM]
status: unread
---

# Oracle-RLAIF: An Improved Fine-Tuning Framework for Multi-modal Video Models through Reinforcement Learning from Ranking Feedback

## Summary

Oracle-RLAIF replaces the trained reward model in RLAIF pipelines with a general Oracle ranker that ranks candidate responses rather than scoring them, eliminating expensive reward model training. It introduces GRPO_rank, a rank-aware variant of GRPO that optimizes ordinal advantages directly from ranking feedback. The framework outperforms leading VLMs on video comprehension benchmarks and generalizes flexibly across model configurations.

## Key Contributions

- Replaces scalar reward model with an Oracle ranker (drop-in ranking model), eliminating reward model training cost
- Introduces GRPO_rank: a novel rank-aware loss extending GRPO to ordinal feedback with rank-weighted advantages
- Demonstrates consistent outperformance over leading VLMs on multiple video comprehension benchmarks
- Provides a more flexible and data-efficient RLAIF pipeline applicable across VLM scales

## Relevance

Connects two core profile interests: RLAIF and GRPO. The insight that ranking is cheaper and more reliable than scoring for AI feedback directly addresses reward model overoptimization concerns, and the GRPO_rank variant is a practical technique for VLM alignment without human labels.

## My Thoughts

<!-- Add your own notes here -->
