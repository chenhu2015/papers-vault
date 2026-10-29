---
title: "Pareto-Dominant Clarification: Post-Training Coding LLMs via PPO-Lagrangian Budget Constraints"
authors: ["Abhinav Rajput", "Acey Vogelstein"]
date: 2026-10-29
arxiv_id: "2610.04089v1"
url: "http://arxiv.org/abs/2610.04089v1"
score: 0.80
topics: [agentic RL, reinforcement learning, PPO, RLHF]
status: unread
---

# Pareto-Dominant Clarification: Post-Training Coding LLMs via PPO-Lagrangian Budget Constraints

## Summary

Formulates clarification behavior in coding agents as a Constrained MDP (CMDP) and post-trains Qwen2.5-Coder-7B via PPO-Lagrangian to maximize coding accuracy subject to an expected question-budget constraint. Budget-constrained policies Pareto-dominate the untuned baseline — achieving higher accuracy and lower clarification rates simultaneously. The resulting log-shaped Pareto frontier reveals that gains come from improved question targeting, not simply asking more questions.

## Key Contributions

- CMDP formulation of agent clarification as an explicit accuracy/efficiency tradeoff with enforceable budget constraints
- PPO-Lagrangian training that eliminates per-budget coefficient tuning (handles all budget levels in one training run)
- Empirical result: budget-constrained policies Pareto-dominate unconstrained baseline on HumanEvalComm
- Emergent non-uniform clarification allocation: policies learn to ask more on harder multi-degradation tasks without explicit supervision

## Relevance

Directly extends the multi-objective/constrained RL thread for LLMs (CoRL from Oct 27 added centralized multi-LLM RL with dual perf/cost objectives; this adds CMDP + PPO-Lagrangian for single-agent clarification budgeting). The CMDP framing is novel relative to prior agentic RL work in the vault which has focused on reward design, not constraint satisfaction.

## My Thoughts

<!-- Add your own notes here -->
