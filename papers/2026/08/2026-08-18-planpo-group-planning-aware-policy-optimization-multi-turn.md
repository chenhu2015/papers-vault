---
title: "PlanPO: Group Planning-Aware Policy Optimization for Multi-Turn Agentic LLMs"
authors: ["Dayang Liang", "Liyuan He", "Xuan Feng", "Shuxin Li"]
date: 2026-08-18
arxiv_id: "2608.17289"
url: "https://arxiv.org/abs/2608.17289"
score: 0.88
topics: [GRPO, agentic RL, LLM agent, PPO, RL training]
status: unread
---

# PlanPO: Group Planning-Aware Policy Optimization for Multi-Turn Agentic LLMs

## Summary

PlanPO fixes a core failure mode of GRPO in multi-turn agentic settings: circuitous and efficient successes receive identical outcome reward, causing advantage collapse. PlanPO introduces coarse-to-fine advantage signals that capture relative trajectory length and turn-level response length conditioned on success, enabling agents to learn generalizable planning behaviors without degenerating into pure length minimization. Improves over GRPO by +27.2% on average across ALFWorld, WebShop, and SciWorld with negligible additional training cost.

## Key Contributions

- Diagnoses advantage collapse in standard GRPO: circuitous and efficient successful trajectories assigned identical reward, eliminating advantage signal within the success group
- Coarse-to-fine advantage signals: trajectory-level length advantage (interaction efficiency) and turn-level response length advantage (generation efficiency), conditioned on success
- +27.2% average improvement over GRPO on three multi-turn benchmarks (ALFWorld, WebShop, SciWorld)
- Negligible additional training cost; operates within the group-relative optimization structure

## Relevance

PlanPO is a direct GRPO extension for multi-turn agentic settings, addressing a failure mode orthogonal to GUPO (Aug 19, gradient aggregation conflicts) and PlanPO together form a two-axis fix for GRPO's failure in multi-turn agents. The advantage collapse diagnosis also connects to RTPO (Aug 20, temporal credit instability) — both papers show that flat trajectory-level signals are insufficient for multi-turn training, but from different angles: RTPO addresses context mismatch and asynchronous drift; PlanPO addresses within-group advantage collapse. The vault's GRPO thread now has: variance reduction (GUPO), advantage discrimination (PlanPO), and temporal stability (RTPO).

## My Thoughts

<!-- Add your own notes here -->
