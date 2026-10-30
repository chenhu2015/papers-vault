---
title: "QwenGyre: An Elastic Reinforcement Learning Framework for Training xLong-Horizon Agents"
authors: ["Weiqi Wang", "Yuxin Zhou", "Mouxiang Chen", "Siyuan Zhang", "Yi Zhang", "Yuyan Luo", "Zhiyu Yin", "Chencan Wu", "Jiemin Jiang", "Wentao Yao", "Chujie Zheng", "JianWei Zhang"]
date: 2026-10-30
arxiv_id: "2609.33848v2"
url: "http://arxiv.org/abs/2609.33848v2"
score: 0.88
topics: [agentic RL, RL training, reinforcement learning]
status: unread
---

# QwenGyre: An Elastic Reinforcement Learning Framework for Training xLong-Horizon Agents

## Summary

QwenGyre is an end-to-end framework for extreme-long-horizon online RL with LLM agents, addressing GPU idling and trajectory redundancy in runs spanning up to 700K tokens per rollout. It elastically reallocates GPUs between rollout and training without interrupting live executions, while a trajectory processor deduplicates redundant branching paths and scores partial progress. Scaled to Qwen 3.8 2.4T on NL2RepoBench, it achieves a 6.0% absolute improvement in 48 steps with up to 1.85× speedup over asynchronous alternatives.

## Key Contributions

- Elastic GPU reallocation between rollout and training phases without interrupting live agent executions
- Trajectory processor that reconstructs branching histories, scores partial progress, and deduplicates redundant paths
- Supports rollouts up to 700K tokens per execution (xlong-horizon SWE/coding tasks) on Qwen 3.8 2.4T (MoE)
- 1.85× and 1.78× speedup over Colocate and Async baselines respectively; 6.0% absolute NL2RepoBench gain

## Relevance

Directly extends the RL rollout efficiency / allocation thread with an extreme-scale infrastructure angle: QwenGyre is the first framework targeting sub-million-token-per-rollout SWE tasks, complementing shorter-horizon rollout selection papers (Nested-ReFT, FlexMARL) with elastic scheduling at maximal scale. The trajectory deduplication mechanism is a novel approach to the redundancy problem in long-horizon branching execution.

## My Thoughts

<!-- Add your own notes here -->
