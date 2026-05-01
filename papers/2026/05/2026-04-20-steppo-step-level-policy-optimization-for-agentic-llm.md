---
title: "StepPO: Step-Level Policy Optimization for Agentic LLM Reinforcement Learning"
authors: []
date: 2026-04-20
arxiv_id: "2604.18401"
url: "https://arxiv.org/abs/2604.18401"
score: 0.92
topics: [agentic-RL, RL-training, tool-use, LLM-agent]
status: unread
---

# StepPO: Step-Level Policy Optimization for Agentic LLM Reinforcement Learning

## Summary

Proposes a step-level MDP for LLM agentic RL where each agent decision (including tool calls) is the optimization unit rather than individual tokens. Introduces step-level credit assignment to handle sparse and delayed rewards in multi-turn tool-use scenarios, making RL training more stable and effective for long-horizon agentic tasks.

## Key Contributions

- Step-level MDP formulation where each tool call or decision step is treated as an action
- Step-level credit assignment to address reward sparsity in multi-turn agentic settings
- Empirical demonstration of more stable training compared to token-level approaches

## Relevance

Directly addresses the core challenge of training agentic LLMs via RL — how to assign credit across long multi-turn tool-use trajectories. Highly relevant to the current focus on agentic RL training.

## My Thoughts

<!-- Add your own notes here -->
