---
title: "Controlling Performance and Budget of a Centralized Multi-agent LLM System with Reinforcement Learning"
authors: ["Bowen Jin", "TJ Collins", "Donghan Yu", "Mert Cemri", "Shenao Zhang", "Mengyu Li", "Jay Tang", "Tian Qin", "Zhiyang Xu", "Jiarui Lu", "Guoli Yin", "Jiawei Han", "Zirui Wang"]
date: 2025-11-04
arxiv_id: "2511.02755"
url: "https://arxiv.org/abs/2511.02755"
score: 0.72
topics: [agentic RL, LLM agent, tool use, reinforcement learning]
status: unread
---

# Controlling Performance and Budget of a Centralized Multi-agent LLM System with Reinforcement Learning

## Summary

CoRL introduces a centralized multi-LLM framework where a controller LLM selectively coordinates a pool of expert models, formulating this as RL with dual objectives — maximising task performance while minimising inference cost — in a controllable multi-budget setting. Unlike decentralised approaches that invoke all models per query, the centralised controller enables a single trained system to adaptively surpass the best individual expert at high budget while maintaining competitive performance at low budget. Experiments on four diverse benchmarks demonstrate consistent cost-performance Pareto improvements over decentralised baselines.

## Key Contributions

- Centralized controller LLM that selectively invokes expert models — replaces always-invoke decentralised routing
- RL formulation with dual objectives: task performance maximisation + inference cost minimisation
- Controllable multi-budget setting: single trained system adapts to different budget constraints at inference time
- Surpasses the best single expert at high-budget; maintains competitive performance at low-budget on 4 benchmarks

## Relevance

Connects to the long-horizon agentic RL thread (Arctic-SWE, CoD, LoongSage) from the system design angle: where LoongSage builds async execution infrastructure for agentic RL, CoRL addresses the model-routing and cost-control layer above it. The multi-budget RL framing also echoes LLMZero's adaptive strategy discovery but applied to agent coordination rather than GRPO hyperparameters.

## My Thoughts

<!-- Add your own notes here -->
