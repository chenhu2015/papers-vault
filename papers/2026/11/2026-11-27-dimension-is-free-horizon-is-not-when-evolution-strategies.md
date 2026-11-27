---
title: "Dimension Is Free, Horizon Is Not: When Evolution Strategies Rival Policy Gradients for LLM Fine-Tuning"
authors: ["Qiyao Liang", "Kajetan Schweighofer", "Xin Qiu", "Risto Miikkulainen"]
date: 2026-11-22
arxiv_id: "2611.29795v1"
url: "https://arxiv.org/abs/2611.29795"
score: 0.9
topics: [agentic RL, RL training, GRPO]
status: unread
---

# Dimension Is Free, Horizon Is Not: When Evolution Strategies Rival Policy Gradients for LLM Fine-Tuning

## Summary

Provides a theoretical framework explaining when Evolution Strategies (ES) outperform policy gradient methods (GRPO) for LLM fine-tuning: ES cost grows with effective dimension (number of independent skills), while PG cost grows with effective horizon (tokens sharing credit with the reward). Empirical comparison on 20 NLP/math/agentic tasks with Qwen2.5-7B confirms PG leads on short-horizon tasks and ties on math, with Terminal-Bench (long-horizon agentic) showing ES surpassing the released Tmax PG checkpoint without any credit assignment. Predicts ES will become increasingly competitive as agentic benchmark horizons lengthen.

## Key Contributions

- Theoretical decomposition: ES noise ∝ effective dimension, PG noise ∝ effective horizon; crossover horizon shifts right as skill count grows
- Synthetic task with independently controllable skill count and horizon validates the theory
- Empirical measurement of effective horizons across 20 NLP/math/agentic benchmarks with Qwen2.5-7B
- Terminal-Bench (long-horizon agentic) preliminary result: ES without credit assignment surpasses the GRPO checkpoint released with Tmax

## Relevance

Directly connects to the ZO/forward-only training thread opened by ARS-VLM — ES is a gradient-free method that now has a principled regime where it beats GRPO, specifically long-horizon agentic tasks. Also intersects the long-horizon agentic RL failure mode thread (RLVB, PROVE, FALCA): credit assignment is what makes GRPO competitive on long horizons, and ES avoids this problem by bypassing credit altogether.

## My Thoughts

<!-- Add your own notes here -->
