---
title: "TIGPO: Temporal Instance-Graph Policy Optimization for Long-Horizon LLM Agents"
authors: ["Jinwei Gan"]
date: 2026-09-03
arxiv_id: "2609.03383v1"
url: "http://arxiv.org/abs/2609.03383v1"
score: 0.88
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# TIGPO: Temporal Instance-Graph Policy Optimization for Long-Horizon LLM Agents

## Summary

TIGPO extends graph-based credit assignment across policy updates by maintaining a persistent transition graph per task, allowing transitions discovered by earlier policy versions to inform advantage estimation for current rollouts. It allocates a fixed rollout budget between fresh Exploration slots and Revisit slots that pair current rollouts with earlier exploration groups, enabling cross-temporal relative advantage estimation without replaying historical data in the policy loss. Evaluated on ALFWorld and WebShop, TIGPO consistently outperforms prior group-based and graph-based policy optimization methods.

## Key Contributions

- Persistent per-task transition graph that accumulates valid transitions across policy updates (unlike GRAFT/SALT which rebuild per-batch)
- Exploration vs. Revisit slot budget split: Revisit slots force re-sampling of earlier explored tasks paired with their historical groups
- Cross-temporal reference construction for enlarged group-level advantage estimation, stabilizing credit under small rollout groups
- Historical transitions serve only as detached statistical references — never replayed in the policy gradient loss

## Relevance

Directly extends the GRAFT/SALT/MileGPO step-level credit cluster by adding temporal persistence: where GRAFT and SALT construct graphs within a single policy update, TIGPO accumulates transitions across updates, addressing the problem of small effective group sizes in sparse-reward tasks. Natural follow-up question: can TIGPO's temporal graph be combined with GRAFT's Bellman/Graph-GAE estimation?

## My Thoughts

<!-- Add your own notes here -->
