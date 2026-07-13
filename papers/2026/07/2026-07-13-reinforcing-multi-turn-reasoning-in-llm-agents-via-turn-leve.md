---
title: "Reinforcing Multi-Turn Reasoning in LLM Agents via Turn-Level Reward Design"
authors: ["Quan Wei", "Siliang Zeng", "Chenliang Li", "William Brown", "Oana Frunza", "Wei Deng", "Anderson Schneider", "Yuriy Nevmyvaka", "Yang Katie Zhao", "Alfredo Garcia", "Mingyi Hong"]
date: 2026-07-13
arxiv_id: "2505.11821v2"
url: "https://arxiv.org/abs/2505.11821"
score: 0.80
topics: [agentic RL, RL training, GRPO, PPO, LLM agent, tool use]
status: unread
---

# Reinforcing Multi-Turn Reasoning in LLM Agents via Turn-Level Reward Design

## Summary

The first systematic study of turn-level reward design for multi-turn RL in LLM agents, extending GRPO and PPO with fine-grained credit assignment via intermediate turn-level rewards. Two reward types are studied in multi-turn search agents: verifiable (rule-based per-turn signal) and LLM-as-judge. Incorporating turn-level rewards achieves greater stability, faster convergence, and higher accuracy than trajectory-level outcome rewards alone across diverse QA benchmarks.

## Key Contributions

- Extends GRPO and PPO to multi-turn variants with turn-level reward integration — first systematic study of this design space
- Two turn-level reward types: verifiable (rule-based) and LLM-as-judge, studied in multi-turn reasoning-augmented search agents
- Turn-level rewards provide greater stability and faster convergence than trajectory-level sparse outcome rewards
- Applied to multi-turn search agents (not just single-turn math reasoning), demonstrating generality to agentic tool-use settings

## Relevance

Directly answers the question from the Jul 12 digest: does HRM's hierarchical consecutive-step evaluation extend to multi-turn agentic settings? This paper shows that turn-level rewards in agentic multi-turn settings (rather than step-level rewards in single-turn math) produce the same credit assignment benefit. Together with HRM ([[2026-07-12-towards-hierarchical-multi-step-reward-models-for-enhanced]]) and OSPO ([[2026-07-11-owen-shapley-policy-optimization-a-principled-rl-algorithm-f]]), this forms a cross-setting picture of fine-grained credit assignment: HRM at the step level for math PRMs, OSPO at the segment level for game-theoretic attribution, and this paper at the turn level for agentic search. The LLM-as-judge turn-level reward type also connects to the agentic tool-use RL framework (DART/ARTIST) where turn-level supervision is hard to obtain verifiably.

## My Thoughts

<!-- Add your own notes here -->
