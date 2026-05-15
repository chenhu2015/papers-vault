---
title: "Language Self-Play For Data-Free Training"
authors: ["Jakub Grudzien Kuba", "Mengting Gu", "Qi Ma", "Yuandong Tian", "Vijai Mohan", "Jason Chen"]
date: 2025-09-09
arxiv_id: "2509.07414"
url: "https://arxiv.org/abs/2509.07414"
score: 0.78
topics: [agentic RL, RL training, reinforcement learning, LLM agent]
status: unread
---

# Language Self-Play For Data-Free Training

## Summary

Language Self-Play (LSP) reframes LLM capability improvement as performance in a competitive two-player game, allowing the model to improve by playing against itself without any additional training data. The game-theoretic framing means stronger policies emerge naturally from self-play dynamics, with no human annotations or verifiable reward signals required. Experiments with Llama-3.2-3B-Instruct on instruction-following, mathematics, and coding benchmarks confirm that self-play alone can meaningfully improve pretrained models.

## Key Contributions

- Game-theoretic formulation of LLM self-improvement as a two-player competitive game
- Data-free training: no additional data, annotations, or verifiable reward signals required
- Demonstrates that competitive game dynamics alone (self-play) are sufficient to elicit capability improvement
- Validated across instruction-following, math, and coding — diverse task domains

## Relevance

The foundational theory paper in the self-play-for-LLMs thread. Where SPIRAL, SeRL, and SPELL all build complex multi-role or multi-game architectures on top of self-play, LSP establishes the minimal viable game-theoretic premise: a model playing itself suffices for improvement. Provides the theoretical bedrock for the other four papers in today's digest.

## My Thoughts

<!-- Add your own notes here -->
