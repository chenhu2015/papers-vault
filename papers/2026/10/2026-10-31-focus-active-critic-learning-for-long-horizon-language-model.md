---
title: "FOCUS: Active Critic Learning for Long-Horizon Language Model Agents"
authors: ["Zhengping Jiang", "William Jurayj", "Liaoyaqi Wang", "Chunsheng Zuo", "Anqi Liu", "Benjamin Van Durme"]
date: 2026-10-31
arxiv_id: "2610.35801v1"
url: "http://arxiv.org/abs/2610.35801v1"
score: 0.87
topics: [agentic RL, reinforcement learning, LLM agent, tool use]
status: unread
---

# FOCUS: Active Critic Learning for Long-Horizon Language Model Agents

## Summary

FOCUS addresses sparse reward credit assignment in long-horizon LM agents with selective branching: a rollout controller samples continuations from states expected to most reduce critic estimation error, providing active learning targets for the critic network. TD(λ) advantage is computed over compaction-induced segment boundaries, and a context-management interface decouples context handling from rollout allocation. On Qwen3.5-9B, FOCUS outperforms GRPO and VinePPO by 7.2 points on BrowseComp-Plus (55.4 vs. 48.2) and 4.1 points on DeonticBench (56.5 vs. 52.4).

## Key Contributions

- Selective branching: rollout controller allocates continuation samples to states with highest expected critic error reduction (active learning for value estimation)
- TD(λ) advantage over compaction-induced segment boundaries — uses context compaction events as natural credit-assignment boundaries
- Context-management interface that decouples context compaction from rollout budget allocation
- Outperforms GRPO and VinePPO on long-horizon legal reasoning (DeonticBench) and deep web search (BrowseComp-Plus)

## Relevance

Directly extends the long-horizon agentic RL thread with a novel answer to the sparse reward credit assignment problem. While RSIPO (Oct 30) addressed credit via skill-policy co-evolution and CORD (Oct 30) handled gradient conflicts, FOCUS tackles the fundamental value estimation inaccuracy problem at the root — the critic cannot learn from sparse outcomes alone, so it actively requests the branches needed to calibrate. Complements the SALT (step-level advantage for long-horizon) thread.

## My Thoughts

<!-- Add your own notes here -->
