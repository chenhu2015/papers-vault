---
title: "EnvACE: Internalizing Environment Dynamics via World Rehearsal for Agentic Reinforcement Learning"
authors: ["Zishan Xu", "Zhiyuan Yao", "Yuxin Chen", "Yifu Guo", "Zhengxi Lu", "Yuquan Lu", "Jinyang Huang", "Yan Xu", "Yasheng Wang", "Weinan Zhang", "Xingshan Zeng", "Weiwen Liu"]
date: 2026-08-08
arxiv_id: "2608.06197v1"
url: "http://arxiv.org/abs/2608.06197v1"
score: 0.80
topics: [agentic RL, tool use, LLM agent, RL training]
status: unread
---

# EnvACE: Internalizing Environment Dynamics via World Rehearsal for Agentic Reinforcement Learning

## Summary

EnvACE proposes world rehearsal as a replacement for external environment interaction during agentic RL training: the policy alternates between acting (generating tool calls) and role-playing the environment (generating the induced response), jointly optimized end-to-end with task-success rewards. This internalizes environment dynamics directly into policy parameters, eliminating dependency on costly real or synthesized execution environments. At test time, the internalized world model enables private pre-execution rehearsal within a fixed budget, yielding further gains without additional external interaction.

## Key Contributions

- World rehearsal: policy plays both actor and environment roles in alternating steps, end-to-end
- Joint optimization with task-success rewards internalizes environment dynamics into policy parameters
- Test-time private rehearsal before committed execution improves performance within a moderate rehearsal budget
- Outperforms environment-scaling baselines on BFCL-v4, τ²-Bench, VitaBench, and FinMCP-Bench; gains consistent across model scales

## Relevance

This paper introduces a fourth structural class in the agentic RL training paradigm: where AXPO modifies rollout sampling (prefix-fixing resampling), RAPO injects retrieved trajectories, and DPEPO makes environment diversity an explicit reward signal, EnvACE eliminates the external environment altogether by internalizing it into the policy itself. The world rehearsal paradigm is structurally novel — the same model parameters serve as both the policy and the environment simulator, removing the environment construction bottleneck entirely. Connects to the Aug 8 environment diversity search thread and extends the taxonomy beyond AXPO/RAPO/DPEPO.

## My Thoughts

<!-- Add your own notes here -->
