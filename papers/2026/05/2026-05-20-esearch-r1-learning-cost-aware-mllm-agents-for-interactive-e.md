---
title: "ESearch-R1: Learning Cost-Aware MLLM Agents for Interactive Embodied Search via Reinforcement Learning"
authors: ["Weijie Zhou", "Xuangtang Xiong", "Ye Tian", "Lijun Yue", "Xinyu Wu", "Wei Li", "Chaoyang Zhao", "Honghui Dong", "Ming Tang", "Jinqiao Wang", "Zhengyou Zhang"]
date: 2026-05-20
arxiv_id: "2512.18571v1"
url: "http://arxiv.org/abs/2512.18571v1"
score: 0.85
topics: [agentic RL, LLM agent, GRPO, tool use, VLM, multimodal]
status: unread
---

# ESearch-R1: Learning Cost-Aware MLLM Agents for Interactive Embodied Search via Reinforcement Learning

## Summary

ESearch-R1 addresses ambiguous-instruction embodied search by unifying dialogue (Ask), episodic memory retrieval (GetMemory), and physical navigation (Navigate) into a single MLLM decision process. HC-GRPO (Heterogeneous Cost-Aware GRPO) samples groups of reasoning trajectories and reinforces those achieving the optimal information-gain-to-cost tradeoff, replacing PPO's separate value critic. On AI2-THOR, ESearch-R1 improves task success rates while reducing total operational costs by ~50% versus ReAct-based agents.

## Key Contributions

- Unified embodied action space: Ask, GetMemory, Navigate treated as a single MLLM decision process with heterogeneous cost accounting
- HC-GRPO: extends GRPO to heterogeneous cost spaces (navigation time, human attention), learning cost-aware policies without a value critic
- 50% reduction in total operational cost while improving task success on AI2-THOR embodied search
- First MLLM to jointly optimize information gain against physical and social costs in interactive embodied environments

## Relevance

Directly bridges the multi-turn agentic tool-use RL thread (May 16 digest: ActFocus, AEM, CM2) with embodied VLM RL (elusive since May 16). HC-GRPO is a meaningful GRPO extension addressing heterogeneous multi-objective costs—distinct from multi-turn reward calibration papers. Also confirms embodied MLLM agents with GRPO are a productive thread worth further searching.

## My Thoughts

<!-- Add your own notes here -->
