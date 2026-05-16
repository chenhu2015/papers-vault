---
title: "Multi-Turn Reinforcement Learning for Tool-Calling Agents with Iterative Reward Calibration"
authors: ["Wachiravit Modecrua", "Krittanon Kaewtawee", "Krittin Pachtrachai", "Touchapon Kraisingkorn"]
date: 2026-05-16
arxiv_id: "2604.02869v1"
url: "http://arxiv.org/abs/2604.02869v1"
score: 0.87
topics: [tool use, agentic RL, GRPO, LLM agent, RLHF, RL training]
status: unread
---

# Multi-Turn Reinforcement Learning for Tool-Calling Agents with Iterative Reward Calibration

## Summary

This paper applies MT-GRPO and GTPO to tool-calling agents, discovering that naive dense per-turn rewards degrade performance by up to 14pp due to reward-advantage misalignment. Iterative Reward Calibration uses empirical discriminative analysis of rollout data to fix the misalignment, enabling a 4B model trained on Tau-Bench to surpass GPT-4.1 and GPT-4o while a 30.5B MoE model approaches Claude Sonnet 4.5 — the first published RL training results on Tau-Bench.

## Key Contributions

- First application of MT-GRPO + GTPO hybrid advantage to tool-calling agents with LLM-based user simulator
- Diagnoses naive dense reward failure: per-turn rewards degrade by 14pp due to reward discriminativeness vs. advantage direction mismatch
- Iterative Reward Calibration: empirical rollout analysis to design discriminative, correctly-directed per-turn rewards
- 4B Qwen3.5 trained model: 66.7% on Tau-Bench, beating GPT-4.1 (49.4%) and GPT-4o (42.8%) despite 50× smaller size

## Relevance

Sits at the intersection of tool use and agentic RL — both core interest profile keywords. The reward misalignment finding is a cautionary generalization of the reward hacking work from May 11, but applied to the multi-turn tool-calling setting specifically. The Tau-Bench results (first published RL training results) make this a landmark paper in the agentic RL for real-world service agents space.

## My Thoughts

<!-- Add your own notes here -->
