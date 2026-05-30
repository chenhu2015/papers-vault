---
title: "Beyond Trajectory Rewards: Step-level Credit Assignment for Agentic Search via Graph Modeling"
authors: ["Yuchen Liu", "Yingjie Feng", "Lixiong Qin", "Jiasi Chen", "Jianing Yu", "Sheng Gao", "Sheng Yang", "Weiran Xu"]
date: 2026-05-28
arxiv_id: "2605.29697"
url: "http://arxiv.org/abs/2605.29697v1"
score: 0.86
topics: [agentic RL, reward model, agentic, LLM agent, RL training]
status: unread
---

# Beyond Trajectory Rewards: Step-level Credit Assignment for Agentic Search via Graph Modeling

## Summary

GDCR treats world knowledge as a latent entity-relation graph and scores each retrieved/cited step by its graph-distance contribution toward the answer node, providing step-level process rewards without costly tree sampling. SAPO then combines GDCR step-level advantages with trajectory-level outcome advantages; experiments across four challenging benchmarks validate consistent effectiveness.

## Key Contributions

- Latent world-graph formulation: knowledge = entity-relation graph, each task = search in latent task graph
- Graph-Distance Contribution Reward (GDCR): scores steps by newly-retrieved/cited entity proximity to answer node
- Step Advantage Policy Optimization (SAPO): hybrid step-level + trajectory-level advantages
- No tree sampling required — training-time ER graph provides the reward structure

## Relevance

Extends the search-augmented RL thread (IG-Search, TIPS, PiCA from May 27–28) with a novel graph-theoretic step reward that doesn't require the expensive tree sampling other methods need; directly relevant to agentic search RL.

## My Thoughts

<!-- Add your own notes here -->
