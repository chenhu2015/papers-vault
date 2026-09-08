---
title: "SAPO: Single-Rollout Autoregressive Policy Optimization for Agentic Reinforcement Learning"
authors: ["Dayang Liang", "Lang Feng", "Bo An", "Yunlong Liu"]
date: 2026-09-08
arxiv_id: "2608.19842v2"
url: "http://arxiv.org/abs/2608.19842v2"
score: 0.82
topics: [agentic RL, RL training, PPO, GRPO, LLM agent]
status: unread
---

# SAPO: Single-Rollout Autoregressive Policy Optimization for Agentic Reinforcement Learning

## Summary

SAPO shares a single autoregressive backbone for policy and value by producing predictions at distinct causal boundaries with shared parameters, independently optimizing PPO and auxiliary on-policy SARSA objectives. A trajectory-level GAE combining lambda-returns with batch normalization robustly estimates per-turn contribution, achieving +15.1%/+12.1% over PPO/GRPO on ALFWorld/WebShop and a 33.2% per-iteration speedup by eliminating the separate critic model.

## Key Contributions

- Shared autoregressive backbone for policy and value at distinct causal boundaries — eliminates separate critic model without sacrificing optimization quality
- Auxiliary on-policy SARSA objective independently optimized alongside PPO for value function accuracy
- Trajectory-level GAE with lambda-returns and batch normalization for robust per-turn contribution estimation
- +15.1%/+12.1% over PPO/GRPO on ALFWorld/WebShop; 33.2% per-iteration speedup vs. PPO

## Relevance

SAPO addresses the memory and compute overhead of value-function-based agentic RL — a structural problem orthogonal to RTPO's turn-level optimization dynamics and HARTS's rollout prefix sharing. The shared-backbone approach converges on the same "eliminate separate critic" insight as SAO (today's 5th paper) but from an architectural angle (shared autoregressive backbone) rather than a sampling angle (single-rollout). Together, SAPO and SAO suggest that critic elimination is a robust efficiency axis in agentic RL.

## My Thoughts

<!-- Add your own notes here -->
