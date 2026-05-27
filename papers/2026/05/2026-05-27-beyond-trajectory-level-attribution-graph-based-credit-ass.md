---
title: "Beyond Trajectory-Level Attribution: Graph-Based Credit Assignment for Agentic Reinforcement Learning"
authors: ["Xin Cheng", "Shuo He", "Lang Feng", "HaiYang Xu", "Ming Yan", "Lei Feng", "Bo An"]
date: 2026-05-27
arxiv_id: "2605.26684v1"
url: "http://arxiv.org/abs/2605.26684v1"
score: 0.90
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# Beyond Trajectory-Level Attribution: Graph-Based Credit Assignment for Agentic Reinforcement Learning

## Summary

GraphGPO aggregates all rollout trajectories into a unified state-transition graph and estimates each state's distance to the task goal using global graph structure. Step-level credit is assigned as a graph-based advantage measuring how much each transition reduces goal distance, providing dense and faithful credit for agentic tasks beyond coarse outcome-only attribution. Achieves state-of-the-art across challenging agentic benchmarks.

## Key Contributions

- Unified state-transition graph built from all rollout trajectories in a GRPO-style group
- Graph-based distance estimation from each state to the task goal using global graph topology
- Graph-based advantage per edge: credit proportional to reduction in goal distance
- State-of-the-art performance on agentic benchmarks with improved training efficiency

## Relevance

Directly addresses the token/step-level credit assignment gap in group RL for LLMs — the exact theme targeted by today's searches as the May 26 carry-forward. The graph-based approach is architecturally distinct from prior PRM/step-reward methods, making it a fresh contribution to the user's agentic RL thread.

## My Thoughts

<!-- Add your own notes here -->
