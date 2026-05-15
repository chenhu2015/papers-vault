---
title: "Chasing Moving Targets with Online Self-Play Reinforcement Learning for Safer Language Models"
authors: ["Mickel Liu", "Liwei Jiang", "Yancheng Liang", "Simon Shaolei Du", "Yejin Choi", "Tim Althoff", "Natasha Jaques"]
date: 2025-06-09
arxiv_id: "2506.07468"
url: "https://arxiv.org/abs/2506.07468"
score: 0.80
topics: [agentic RL, RLHF, RL training, reinforcement learning, LLM agent]
status: unread
---

# Chasing Moving Targets with Online Self-Play Reinforcement Learning for Safer Language Models

## Summary

Self-RedTeam frames LM safety alignment as a two-player zero-sum game where a single model alternates between attacker and defender roles, co-evolving via RL with a reward LM adjudicating outcomes. Unlike static red-teaming, the online co-adaptation ensures attackers never overfit to stale defenses, with Nash Equilibrium convergence providing a formal safety guarantee. The method achieves +65.5% robustness on WildJailBreak and +21.8% adversarial diversity over static-defender baselines, with hidden chain-of-thought boosting both attack diversity and reducing over-refusals.

## Key Contributions

- Self-play zero-sum game formulation for safety alignment, unifying attacker and defender into one model
- Formal Nash Equilibrium safety guarantee: at NE, defender reliably produces safe responses to any adversarial input
- Hidden chain-of-thought mechanism enabling private planning for both attacker and defender roles
- +65.5% robustness on WildJailBreak, +21.8% SBERT adversarial diversity over static red-teaming

## Relevance

Connects the RLHF alignment thread to the self-play and multi-agent RL threads emerging today. The zero-sum game framing with a reward LM judge parallels SPIRAL's approach but applies it to safety rather than reasoning — two complementary uses of the same self-play RL paradigm. The hidden CoT addition is an interesting twist on standard RLHF policy training.

## My Thoughts

<!-- Add your own notes here -->
