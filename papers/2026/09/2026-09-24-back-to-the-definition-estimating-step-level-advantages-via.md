---
title: "Back to the Definition: Estimating Step-Level Advantages via Trajectory Graphs for Agentic Reinforcement Learning"
authors: ["Xincheng Yao", "Haobo Fu", "Weiming Liu", "Chongyang Zhang"]
date: 2026-09-24
arxiv_id: "2609.28963v1"
url: "https://arxiv.org/abs/2609.28963"
score: 0.93
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# Back to the Definition: Estimating Step-Level Advantages via Trajectory Graphs for Agentic Reinforcement Learning

## Summary

GRAFT addresses the systematic bias in GRPO's step-level advantage estimation by constructing a trajectory graph from all rollout trajectories and recovering per-node state values via Bellman iteration, assigning per-edge credit as the node value difference. It further proposes Graph GAE to reduce state-value estimation bias, faithfully adhering to the foundational RL advantage definition at the step level. Experiments on multi-turn agentic benchmarks show consistent gains over GRPO and superiority over recent agentic RL algorithms.

## Key Contributions

- Diagnoses why GRPO's group-normalized advantage is reliable at the response level but systematically biased at the step level: trajectory-level advantages cannot accurately reflect individual step contributions, and failed trajectories may contain valuable steps
- Proposes GRAFT: grafts all rollout trajectories into a trajectory graph, recovers node state-values via Bellman iteration on the graph, and assigns per-edge credit by node value differences — faithfully extending the basic RL advantage definition to the step level
- Introduces Graph GAE, which extends Generalized Advantage Estimation (GAE) to the trajectory graph to reduce state-value estimation bias
- Demonstrates consistent gains over GRPO and superior performance compared to recent agentic RL algorithms across multi-turn agentic benchmarks

## Relevance

Directly fills the step-level credit attribution gap identified across multiple prior digests (STEPO in EvoCUA-1.5, ECHO turn-selective memory). GRAFT and SALT (2510.20022v1) form a convergent pair — both use trajectory graphs for step-level credit in GRPO, with GRAFT adding the principled Bellman + Graph GAE foundation. Together they close a key open gap: how to provide dense, faithful credit signals for agentic RL without a critic model.

## My Thoughts

<!-- Add your own notes here -->
