---
title: "Maximizing Rollout Informativeness under a Fixed Budget: A Submodular View of Tree Search for Tool-Use Agentic Reinforcement Learning"
authors: ["Yuelin Hu", "Zhenbo Yu", "Zhengxue Cheng", "Wei Liu", "Li Song"]
date: 2026-05-06
arxiv_id: "2605.05262v1"
url: "http://arxiv.org/abs/2605.05262v1"
score: 0.82
topics: [agentic RL, tool use, GRPO, RL training, LLM agent]
status: unread
---

# Maximizing Rollout Informativeness under a Fixed Budget: A Submodular View of Tree Search for Tool-Use Agentic Reinforcement Learning

## Summary

This paper formalizes Rollout Informativeness under a Fixed Budget (RIFB) for tool-use GRPO and proves budget-agnostic independent samplers suffer guaranteed collapse on hard prompts. It recasts intermediate-state selection as monotone submodular maximization (greedy yields 1−1/e guarantee), deriving Uncertainty-aware Upper Confidence Bound (UUCB) as closed-form marginal gains. InfoTree, the resulting training-time tree search framework, adds an Adaptive Budget Allocator that rescues hard prompts and Speculative Expansion for low overhead. Evaluated across nine benchmarks spanning AIME, GAIA, BrowseComp, APPS, and AgentBench-OS, InfoTree outperforms flat GRPO and five tree-search baselines.

## Key Contributions

- Formal proof that budget-agnostic samplers collapse on hard prompts regardless of budget size
- Submodular reformulation of intermediate-state selection with UUCB as the closed-form greedy selector
- Adaptive Budget Allocator rescues hard prompts (mixed-outcome ratio: 58.1% → 76.3%) with <5% budget overhead
- Speculative Expansion reduces wall-clock overhead from 14.3% to 4.8%; orthogonal to rollout reuse and trajectory re-weighting

## Relevance

Connects the token-budget RL thread to the agentic tool-use cluster (ParaVT, HyperEyes, GROW from May 22–23); the submodular theory lens is entirely novel among the RL methods digested so far and covers web search + OS agent benchmarks not previously seen.

## My Thoughts

<!-- Add your own notes here -->
