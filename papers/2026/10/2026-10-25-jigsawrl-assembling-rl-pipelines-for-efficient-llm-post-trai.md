---
title: "JigsawRL: Assembling RL Pipelines for Efficient LLM Post-Training"
authors: ["Zhengding Hu", "Hehua Ouyang", "Chang Chen", "Zaifeng Pan", "Yue Guan", "Zhongkai Yu", "Zhen Wang", "Steven Swanson", "Yufei Ding"]
date: 2026-10-25
arxiv_id: "2604.23838v1"
url: "http://arxiv.org/abs/2604.23838v1"
score: 0.79
topics: [RL training, reinforcement learning, agentic RL]
status: unread
---

# JigsawRL: Assembling RL Pipelines for Efficient LLM Post-Training

## Summary

JigsawRL introduces Pipeline Multiplexing as a new parallelism dimension for LLM RL post-training, decomposing each pipeline into a Sub-Stage Graph that exposes hidden intra-stage and inter-worker imbalance. It resolves interference through dynamic resource allocation, migrates long-tail rollouts, and schedules with a look-ahead heuristic. Achieves 1.85× throughput over Verl on synchronous RL and 1.54× over StreamRL/AReaL on asynchronous RL across 4–64 H100/A100 GPUs.

## Key Contributions

- Pipeline Multiplexing: new dimension of RL parallelism beyond data/model/pipeline standard dimensions
- Sub-Stage Graph: decomposes each stage to expose intra-stage and inter-worker imbalance hidden at stage level
- Dynamic resource allocation for multiplexing interference resolution
- Long-tail rollout migration via look-ahead heuristic scheduling
- 1.85× throughput over Verl (sync RL); 1.54× over StreamRL/AReaL (async RL); supports heterogeneous pipelines

## Relevance

Directly extends the Arctic-SWE infrastructure thread (Oct 24): where Arctic-SWE showed that engineering hygiene explains most reported gains in agentic RL, JigsawRL provides the system-level substrate — pipeline multiplexing addresses the imbalance that async rollout systems like Arctic-SWE's encounter at scale. The two papers together describe infrastructure at different levels (training loop vs. pipeline scheduling).

## My Thoughts

<!-- Add your own notes here -->
