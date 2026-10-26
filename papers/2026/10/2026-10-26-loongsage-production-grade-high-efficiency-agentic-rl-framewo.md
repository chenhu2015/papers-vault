---
title: "LoongSage: A Production-Grade, High-Efficiency Agentic RL Framework for Frontier LLMs with Validated Recipes"
authors: ["LoongSage Team", "Bowei Song", "Caiwei Zhao", "Chuwen Liu", "Dechuang Gu", "Dong Fang", "Feiyu Xie", "Huaiyu Li", "Hui Zhang"]
date: 2026-10-12
arxiv_id: "2610.16352v2"
url: "http://arxiv.org/abs/2610.16352v2"
score: 0.87
topics: [agentic RL, RL training, LLM agent, tool use]
status: unread
---

# LoongSage: A Production-Grade, High-Efficiency Agentic RL Framework for Frontier LLMs with Validated Recipes

## Summary

LoongSage is a fully asynchronous, agent-native RL framework (~14K LOC) built on Megatron and SGLang, targeting long-horizon agentic tasks with external tool invocation and multi-turn interactions. It introduces AgentFlow as a unified execution paradigm for both white-box and black-box agents, TransferMesh for topology-aware weight synchronization, and sliding-window staleness bounding for async trajectories. Extensive evaluations across four training runs show steady task reward improvement while sustaining hardware utilization by eliminating synchronous idle bubbles.

## Key Contributions

- AgentFlow: unified execution paradigm orchestrating white-box and black-box agents under one controller
- TransferMesh: topology-aware weight synchronization routing weights over fastest available transport after each step
- Sliding-window trajectory staleness bounding for fully async rollout pipelines
- Memory-efficient Teacher Manager enabling Multi-Teacher On-Policy Distillation decoupled from GPU memory constraints

## Relevance

Directly advances the long-horizon agentic RL infrastructure thread (Arctic-SWE, JigsawRL) by providing a production-grade, fully asynchronous system with validated training recipes — where prior work identified engineering hygiene as the dominant factor, LoongSage codifies it in a reusable framework. The Agent-Flow abstraction for black-box agents is directly relevant to the LLM agent + tool use cluster.

## My Thoughts

<!-- Add your own notes here -->
