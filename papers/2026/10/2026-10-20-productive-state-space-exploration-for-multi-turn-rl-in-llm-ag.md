---
title: "Productive State-Space Exploration for Multi-turn RL in LLM Agents"
authors: ["Mohammed Haroon Dupty", "Yong Liang Goh", "Song Guo", "Wee Sun Lee"]
date: 2026-10-19
arxiv_id: "2610.25957"
url: "https://arxiv.org/abs/2610.25957"
score: 0.82
topics: [agentic RL, RL training, LLM agent]
status: unread
---

# Productive State-Space Exploration for Multi-turn RL in LLM Agents

## Summary

Proposes a conditional state-space exploration framework for multi-turn LLM agent RL that adds an intrinsic reward penalizing actions whose resulting observation duplicates prior state memory, reducing repetitive invalid-action loops without requiring a general information-theoretic measure. The method addresses the mismatch between the agent's internal state representation and environment dynamics — agents become trapped in high-confidence but unproductive behaviors that violate environment preconditions. Substantially improves policy learning and state-space coverage in multi-turn agentic benchmarks.

## Key Contributions

- Identifies two failure modes in multi-turn LLM agent RL: invalid actions (violating environment preconditions) and cyclical behaviors (repetitive high-confidence actions providing no progress)
- Conditional state-space exploration framework that balances task completion with intrinsic information-seeking behavior
- Intrinsic reward that penalizes actions whose observation duplicates prior state memory — lightweight, no information-theoretic overhead
- Strong empirical results reducing invalid-action rate and action loops in multi-turn environments

## Relevance

Fills a gap in the agentic RL thread that hasn't been searched recently — specifically the exploration problem in multi-turn RL, distinct from the credit assignment focus of most prior entries. Connects to StructRL (Oct 18, long-horizon VLA RL) and CoD (Oct 20, long-lifecycle agents), but attacks the exploration bottleneck rather than the reward structure. The intrinsic curiosity framing also links to Connect the Dots' continuous environment self-updating.

## My Thoughts

<!-- Add your own notes here -->
