---
title: "UnifiedPlayers: Enhance Tool-Integrated Reasoning in Agentic Reinforcement Learning"
authors: ["Wenjie Liao", "Liangjie Zhao", "Zehong Cao"]
date: 2026-09-17
arxiv_id: "2609.20089v1"
url: "http://arxiv.org/abs/2609.20089v1"
score: 0.80
topics: [agentic RL, GRPO, tool use, LLM agent]
status: unread
---

# UnifiedPlayers: Enhance Tool-Integrated Reasoning in Agentic Reinforcement Learning

## Summary

UnifiedPlayers proposes a cooperative three-player framework for self-evolving tool-integrated agentic RL: a Planning Player generates tasks, an Execution Player produces multi-turn trajectories with Python tool calls, and an Evaluation Player constructs executable verifiers. Role-specific GRPO rewards coordinate all three toward a shared objective; the learned verifier reaches 84.2% adversarial detection accuracy and 2.03× higher per-question reward variance than a self-consistency baseline. On twelve reasoning benchmarks, UnifiedPlayers outperforms the strongest prior baseline by at least 3.5% on math and 3.9% on general reasoning.

## Key Contributions

- Cooperative three-player decomposition: Planning/Execution/Evaluation co-trained under a shared GRPO objective
- Role-specific reward design: each player receives rewards aligned with its specialized function
- Adaptive verifier construction by the Evaluation Player — overcomes static verifier limitations in prior self-evolving methods
- 84.2% adversarial detection accuracy and 2.03× reward variance improvement demonstrate verifier quality

## Relevance

Directly relevant to tool use and agentic RL with GRPO. Addresses a gap in EvoHarness-style self-evolving methods (Sep 7 vault) where task generation and evaluation remain static or separated; UnifiedPlayers jointly co-evolves all three components. The Evaluation Player's learned verifier is adjacent to the Coverage/Not-Targeting framework (Sep 17 vault) — both ask how to measure and reward agent progress with non-static signal.

## My Thoughts

<!-- Add your own notes here -->
