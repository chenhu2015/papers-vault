---
title: "Beyond Trajectory-Level Attribution: Graph-Based Credit Assignment for Agentic Reinforcement Learning"
authors: ["Xin Cheng", "Shuo He", "Lang Feng", "HaiYang Xu", "Ming Yan", "Lei Feng", "Bo An"]
date: 2026-06-30
arxiv_id: "2605.26684"
url: "http://arxiv.org/abs/2605.26684v2"
score: 0.81
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# Beyond Trajectory-Level Attribution: Graph-Based Credit Assignment for Agentic Reinforcement Learning

## Summary

Group-based RL methods rely on coarse trajectory-level credit attribution tied to final outcomes, losing fine-grained step contributions — especially valuable steps obscured inside failed trajectories. GraphGPO aggregates all rollout trajectories into a unified state-transition graph and uses the global graph structure to estimate each state's distance to the task goal, computing a graph-based advantage per step based on how much the transition reduces that distance — providing cross-trajectory credit signal unavailable to any single trajectory. GraphGPO significantly improves training efficiency and achieves state-of-the-art on multiple challenging agentic benchmarks.

## Key Contributions

- Aggregates all rollout trajectories in a group into a unified state-transition graph
- Estimates each state's distance to the task goal using global graph structure (not per-trajectory outcomes)
- Graph-based per-step advantage captures value of steps inside failed trajectories that moved toward the goal
- SOTA on multiple agentic benchmarks with significantly improved training efficiency

## Relevance

GraphGPO is the cross-trajectory complement to SCPO (Jun 30): SCPO rescues failed-trajectory steps by finding successful siblings that made the same progress, while GraphGPO rescues them by estimating goal-distance reduction from the global rollout graph. Both attack the same structural problem — trajectory-outcome-dependent credit loses intra-trajectory quality information — but at different granularities (pairwise sibling matching vs. global graph distance). GraphGPO also connects to the credit assignment hierarchy (AT-RL token-level Jun 14, DRE trajectory-segment Jun 19, HiMPO action-type Jun 18): it adds a fourth axis, cross-trajectory state reachability, as the credit signal.

## My Thoughts

<!-- Add your own notes here -->
