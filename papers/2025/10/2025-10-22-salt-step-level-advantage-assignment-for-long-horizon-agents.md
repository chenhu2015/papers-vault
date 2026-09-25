---
title: "SALT: Step-level Advantage Assignment for Long-horizon Agents via Trajectory Graph"
authors: ["Jiazheng Li", "Yawei Wang", "David Yan", "Yijun Tian", "Zhichao Xu", "Huan Song", "Panpan Xu", "Lin Lee Cheong"]
date: 2025-10-22
arxiv_id: "2510.20022v1"
url: "https://arxiv.org/abs/2510.20022"
score: 0.87
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# SALT: Step-level Advantage Assignment for Long-horizon Agents via Trajectory Graph

## Summary

SALT is a plug-and-play step-level credit assignment framework for GRPO-style group-based RL on long-horizon tasks. It constructs a trajectory graph from rollouts of the same prompt and quantifies per-step quality to assign finer-grained advantages without requiring a critic model or modifying the rollout procedure. Evaluation on WebShop, ALFWorld, and AppWorld across multiple model sizes shows consistent improvement over standard GRPO.

## Key Contributions

- Identifies that GRPO's uniform advantage assignment across all steps within a trajectory conflates beneficial and detrimental actions, causing training instability and suboptimal policies on long-horizon tasks
- Constructs a trajectory graph from rollouts of the same prompt to quantify per-step quality and assign step-level advantages using only outcome rewards — no critic model required
- Designed as a plug-and-play module: integrates with existing group-based RL algorithms with no modifications to rollout procedure and negligible computational overhead
- Achieves consistent improvement over GRPO on WebShop, ALFWorld, and AppWorld across multiple model sizes, with thorough ablation analysis

## Relevance

SALT is the earlier (Oct 2025) instantiation of the trajectory-graph-for-step-credit idea, predating GRAFT (Sep 2026) by about a year. Read together with [[2026-09-24-back-to-the-definition-estimating-step-level-advantages-via]], they form a complementary pair: SALT establishes the trajectory-graph plug-in approach and validates it on agentic benchmarks; GRAFT adds the principled Bellman iteration + Graph GAE foundation. Together they close the step-level credit attribution gap that STEPO (EvoCUA-1.5) and ECHO approached from different angles.

## My Thoughts

<!-- Add your own notes here -->
