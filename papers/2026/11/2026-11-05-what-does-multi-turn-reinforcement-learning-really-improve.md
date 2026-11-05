---
title: "What Does Multi-Turn Reinforcement Learning Really Improve in LLM Agents?"
authors: ["Kejian Zhu", "Zhuoran Jin", "Shangqing Tu", "Tianyi Men", "Yupu Hao", "Jiachun Li", "Kang Liu", "Jun Zhao"]
date: 2026-11-04
arxiv_id: "2611.06483v1"
url: "http://arxiv.org/abs/2611.06483v1"
score: 0.82
topics: [agentic RL, LLM agent, reinforcement learning, GRPO]
status: unread
---

# What Does Multi-Turn Reinforcement Learning Really Improve in LLM Agents?

## Summary

A Pass@(K,T) evaluation framework separating sampling breadth K from interaction depth T reveals that multi-turn agentic RL performance gains are strongly turn-budget-dependent: advantages diminish significantly under tight interaction constraints, and RL selectively strengthens error recovery and long-horizon resilience rather than uniformly improving single-step decision quality. BudgetMix RL varies interaction budgets during training to achieve deployment-robust performance across diverse execution settings.

## Key Contributions

- Pass@(K,T) metric disentangles sampling breadth from interaction depth, exposing budget-sensitivity of agentic RL gains
- Key finding: RL concentrates improvements in error recovery and long-horizon resilience, not step-level decision quality
- Identifies turn-budget dependence as a deployment risk: gains achieved under generous budgets don't transfer under tight budgets
- BudgetMix RL: trains across varied turn budgets to achieve robustness across deployment settings

## Relevance

Important diagnostic paper for the long-horizon agentic RL thread; the finding that RL improves error recovery rather than step quality recasts the role of agentic RL training (correction vs. anticipation). Pairs well with SCOPE (Nov 2, selective step distillation at error steps) — SCOPE optimizes exactly the error-recovery mechanism that this paper shows RL improves.

## My Thoughts

<!-- Add your own notes here -->
