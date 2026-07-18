---
title: "Information Gain-based Rollout Policy Optimization: An Adaptive Tree-Structured Rollout Approach for Multi-Turn LLM Agents"
authors: ["Yijun Zhang", "Fan Xu", "Jiaxin Ding", "Yule Xie", "Shiqing Gao", "Xin Ding", "Haoxiang Zhang", "Luoyi Fu", "Xinbing Wang"]
date: 2026-07-07
arxiv_id: "2607.06223"
url: "https://arxiv.org/abs/2607.06223"
score: 0.85
topics: [agentic RL, LLM agent, RL training, reinforcement learning, tool use]
status: unread
---

# Information Gain-based Rollout Policy Optimization: An Adaptive Tree-Structured Rollout Approach for Multi-Turn LLM Agents

## Summary

Proposes IGRPO, a policy optimization framework that treats intermediate-state informativeness as the organizing principle for rollout budget allocation in multi-turn LLM agents. Budget-aware tree-structured rollouts allocate expansion budget by node-level information gain — expanding promising branches more frequently and suppressing unpromising ones — with the information gain rollout inducing an explicit limiting teacher distribution over trajectories that yields a principled policy optimization target. Outperforms strong baselines on seven search-augmented QA benchmarks under the same rollout budget constraints.

## Key Contributions

- Identifies core limitation: existing rollout methods allocate budget without assessing intermediate-state utility, wasting compute on low-value branches
- Budget-aware tree-structured rollouts: expansion budget allocated by node-level information gain (informativeness); promising branches expanded more, unpromising branches progressively suppressed
- Information gain-based rollout induces explicit limiting teacher distribution over trajectories — unifying adaptive exploration with principled policy learning under single framework
- Consistent outperformance on seven search-augmented QA benchmarks under fixed rollout budget constraints

## Relevance

Directly extends the agentic TTS thread (TTI, Scaling TTS for Agents, General AgentBench, Learning When to Plan) to the rollout design level: TTI showed curriculum RL on rollout *horizon* is the right axis; IGRPO shows *which branches* to expand within that horizon via information gain is equally important. The induced teacher distribution unification is the cleanest theoretical integration between tree-search-based exploration and RL policy optimization seen in the vault.

## My Thoughts

<!-- Add your own notes here -->
