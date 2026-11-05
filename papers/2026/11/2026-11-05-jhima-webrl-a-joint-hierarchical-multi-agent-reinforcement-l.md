---
title: "JHiMA-WebRL: A Joint Hierarchical Multi-Agent Reinforcement Learning Framework for Long-Horizon Web Tasks"
authors: ["Shanka Subhra Mondal", "Jiayun Wang"]
date: 2026-11-03
arxiv_id: "2611.05263v1"
url: "http://arxiv.org/abs/2611.05263v1"
score: 0.83
topics: [agentic RL, GRPO, LLM agent, tool use]
status: unread
---

# JHiMA-WebRL: A Joint Hierarchical Multi-Agent Reinforcement Learning Framework for Long-Horizon Web Tasks

## Summary

JHiMA-WebRL jointly trains a hierarchical planner and executor via GRPO with hierarchical rollout grouping and role-specific advantages for long-horizon web navigation. A strong teacher model bootstraps structured subtask supervision from multimodal GUI trajectories; RL then jointly optimizes both roles in WebArena, where JHiMA-WebRL-14B (7B+7B) reaches 37.2% vs. 24% for a 32B monolithic RL baseline. The key insight is that jointly learned role factorization with smaller specialized models outperforms scaling a monolithic agent.

## Key Contributions

- Separate task decomposer (planner) and subtask-conditioned actor (executor) jointly trained end-to-end
- Teacher-guided bootstrapping via strong model annotation of subtask structure from multimodal GUI trajectories
- GRPO extended to joint hierarchical optimization with hierarchical rollout grouping and role-specific advantages
- 37.2% on WebArena-Lite-v2 vs. 24% for a ScaleCUA-32B fine-tuned with RL; jointly updating decomposer during RL outperforms actor-only updates

## Relevance

Directly advances the long-horizon agentic RL and multi-agent LLM RL threads; the hierarchical role factorization approach via joint GRPO optimization is a new answer to the monolithic-vs-modular tradeoff, complementing CoHARL's harness co-evolution and SCOPE's selective step distillation.

## My Thoughts

<!-- Add your own notes here -->
