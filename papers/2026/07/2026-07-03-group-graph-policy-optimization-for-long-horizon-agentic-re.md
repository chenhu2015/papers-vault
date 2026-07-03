---
title: "Group-Graph Policy Optimization for Long-Horizon Agentic Reinforcement Learning"
authors: ["Yunan Wang", "Minghui Song", "Zihan Zhang", "Shaohan Huang", "Haizhen Huang", "Furu Wei", "Weiwei Deng", "Feng Sun", "Qi Zhang"]
date: 2026-06-22
arxiv_id: "2606.22995v1"
url: "http://arxiv.org/abs/2606.22995v1"
score: 0.91
topics: [agentic RL, RL training, GRPO]
status: unread
---

# Group-Graph Policy Optimization for Long-Horizon Agentic Reinforcement Learning

## Summary

G2PO transforms linear agentic interaction trajectories into a global state-transition graph, enabling group-aggregation state-value estimation that reduces sampling variance by merging identical observations across rollouts. Edge-centric advantage estimation standardizes TD errors globally across the graph to explicitly identify and prioritize critical state transitions, improving over GRPO by up to +22.2% on WebShop, ALFWorld, and AppWorld.

## Key Contributions

- Explicit transformation of linear rollout trajectories into a global state-transition graph; identical observations across trajectories are merged into shared nodes
- Group-aggregation state-value estimation: aggregating returns from all trajectories visiting a state node reduces per-trajectory variance and trajectory-dependent bias
- Edge-centric advantage estimation: redefines actions as state-node transitions and globally standardizes TD errors across the entire graph to surface "critical transitions"
- +22.2% over GRPO on WebShop and consistent improvements on ALFWorld and AppWorld without requiring a learned value network

## Relevance

G2PO extends the graph-based credit thread (GraphGPO, RewardFlow) into the GRPO training algorithm itself — where GraphGPO used prospective goal-distance on the rollout graph and RewardFlow used retrospective propagation, G2PO builds the graph directly into the advantage estimator via group-aggregation and global TD standardization. The edge-centric advantage (identifying which state transitions matter most) is the closest operational analogue to RewardFlow's topology-aware propagation yet evaluated within a GRPO training loop.

## My Thoughts

<!-- Add your own notes here -->
