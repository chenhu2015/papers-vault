---
title: "HARTS: Efficient Agentic Reinforcement Learning for Hybrid-Attention Models over Arbitrary Rollout Trees"
authors: ["Boyuan Meng", "Peihua Bao", "Hong Liu", "Xiaowei Zhu", "Chao Wang", "Gen Li", "Zhenxuan Pan"]
date: 2026-08-28
arxiv_id: "2608.28158"
url: "http://arxiv.org/abs/2608.28158v1"
score: 0.78
topics: [agentic RL, RL training, LLM agent]
status: unread
---

# HARTS: Efficient Agentic Reinforcement Learning for Hybrid-Attention Models over Arbitrary Rollout Trees

## Summary

HARTS addresses the training inefficiency of agentic RL's irregular rollout trees by jointly planning microbatches and data-parallel assignments with non-replay compact-token work after prefix compression, avoiding redundant recomputation of shared prefixes across branches. For hybrid attention models it extends this with a linear-time chunk-boundary state recovery algorithm and differentiable state handoffs, achieving 4.81–4.87x forward/backward/gradient speedup on SWE-bench agentic RL workloads.

## Key Contributions

- Jointly plans microbatches, data-parallel replica assignments, and microbatch-slot schedules using non-replay compact-token work after prefix compression
- Linear-time algorithm for chunk-boundary state recovery and replay in chunkwise linear attention, minimizing sequential linear-attention calls
- Differentiable state handoffs supporting activation recomputation and semantic MoE weight restoration
- 4.81–4.87x forward/backward/gradient speedup on SWE-bench agentic RL with numerical differences comparable to baseline self-rerun variation

## Relevance

HARTS solves the systems bottleneck that constrains agentic RL at scale: irregular rollout trees with shared prefixes incur O(N) redundant recomputation without prefix sharing, which compounds with TeamTR's O(N²) compounding occupancy shift problem in multi-agent settings. HARTS + TeamTR together form a complementary pair: TeamTR controls the policy-stale data problem across agents; HARTS controls the compute-redundancy problem within each agent's rollout tree. The hybrid-attention extension is particularly relevant as the vault's agentic RL papers (GBT, EDGE, AToD) are likely to move to hybrid-attention architectures as they scale.

## My Thoughts

<!-- Add your own notes here -->
