---
title: "RODS: Reward-Driven Online Data Synthesis for Multi-Turn Tool-Use Agents"
authors: ["Ruishan Fang", "Siyuan Lu", "Chenyi Zhuang", "Tao Lin"]
date: 2026-06-18
arxiv_id: "2606.19047"
url: "https://arxiv.org/abs/2606.19047"
score: 0.84
topics: [agentic RL, GRPO, tool use, LLM agent]
status: unread
---

# RODS: Reward-Driven Online Data Synthesis for Multi-Turn Tool-Use Agents

## Summary

Multi-turn tool-use RL depletes informative training samples as the policy improves, because GRPO gradient signal concentrates on samples at the agent's capability boundary (highest rollout reward variance, per the Popoviciu bound). RODS repurposes this reward variance signal as a zero-cost boundary detector, then synthesizes new multi-turn tool-use variants that match the structural complexity of boundary samples (API topology, dependency depth) via a skill-aligned resampling pipeline and a co-evolving dynamic replay buffer. Starting from 400 human seeds, RODS matches a 17K-sample offline pipeline while requiring roughly 20× fewer trajectories.

## Key Contributions

- Identifies boundary sample depletion as the core failure mode in static-dataset GRPO for tool-use agents, grounded in the Popoviciu variance bound
- Uses rollout reward variance as a zero-overhead boundary detector — no extra inference beyond what GRPO already computes
- Skill-aligned resampling synthesizes new multi-turn variants matching the API topology and dependency depth of detected boundary samples
- Dynamic replay buffer co-evolves with the policy, maintaining a live training pool of ~800 samples equivalent to a 17K static dataset

## Relevance

Directly extends the GRPO tool-use training thread (ToolRLA Jun 12, SENTINEL Jun 12, PathRouter Jun 17) with a data-side solution to sample depletion — the Popoviciu boundary-detection insight is a clean complement to TRACE (Jun 11)'s rollout budget allocation, which addressed compute efficiency; RODS addresses data efficiency for the same class of tasks.

## My Thoughts

<!-- Add your own notes here -->
