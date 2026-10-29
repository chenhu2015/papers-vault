---
title: "FlexMARL: Graph-Driven Rollout-Training Co-Design for LLM-Based Multi-Agent Reinforcement Learning"
authors: ["Zhida Jiang", "Zhaolong Xing", "Jiawei Lu", "Yipei Niu", "Qingyuan Sang", "Liangxu Zhang", "Wenquan Dai", "Junhua Shu", "Jiaxing Wang", "Qiangyu Pei", "Qiong Chen", "Xinyu Liu", "Fangming Liu", "Ai Han", "Zhen Chen", "Ke Zhang"]
date: 2026-10-29
arxiv_id: "2602.09578v2"
url: "http://arxiv.org/abs/2602.09578v2"
score: 0.70
topics: [agentic RL, RL training, reinforcement learning, LLM agent]
status: unread
---

# FlexMARL: Graph-Driven Rollout-Training Co-Design for LLM-Based Multi-Agent Reinforcement Learning

## Summary

FlexMARL introduces a Multi-Agent Execution Graph (MEG) abstraction and co-designs rollout and training engines for large-scale LLM-based MARL. The Rollout Engine uses dependency-parallel sampling with hierarchical load balancing to reduce inference latency and balance intra/inter-agent loads, while the Training Engine enables on-demand per-agent resource allocation. Achieves up to 7.3× speedup and 5.6× hardware utilization improvement over existing frameworks on a production cluster.

## Key Contributions

- Multi-Agent Execution Graph (MEG): intermediate representation that captures dependency structure among agents; materialized as MEG Store for decentralized multi-table storage
- Rollout Engine with dependency-parallel sampling and hierarchical load balancing (intra-agent + inter-agent)
- Agent-level asynchronous pipeline in Joint Orchestrator mitigates critical path synchronization barriers
- Training Engine with on-demand per-agent resource allocation via location-agnostic communication APIs

## Relevance

Infrastructure-level complement to the RL rollout efficiency cluster: while most cluster papers focus on which rollouts to use (I-PPO, LEEPS, TrajVal, ADS), FlexMARL addresses how to execute and schedule rollouts at system level in multi-agent settings. Relevant to the long-horizon agentic RL thread where multi-agent coordination and rollout management at scale becomes a bottleneck.

## My Thoughts

<!-- Add your own notes here -->
