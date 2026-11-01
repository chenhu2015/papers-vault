---
title: "Uni-Mem: Learning a Long-Horizon Agentic Memory Manager with Unified Online Policy Optimization"
authors: ["Zhiqian Xia", "Jielong Tang", "Ling-An Zeng", "Shixiong Kai", "Rong Yao", "Hao Kong", "Xiao Dong", "Wei Wang", "Mingxuan Yuan", "Siyu Xia", "Haifeng Xia"]
date: 2026-11-01
arxiv_id: "2610.29671v1"
url: "https://arxiv.org/abs/2610.29671"
score: 0.85
topics: [agentic RL, RL training, GRPO, LLM agent, RLHF]
status: unread
---

# Uni-Mem: Learning a Long-Horizon Agentic Memory Manager with Unified Online Policy Optimization

## Summary

Trains memory construction and retrieval jointly under a single online RL policy (Uni-Mem) using two new techniques: Stage-Decoupled GRPO, which alternates construction/retrieval optimization while holding the other stage fixed within each rollout group to yield clean per-stage learning signals, and Event-Wise Credit Assignment (ECA), which localizes sparse feedback to responsible memory events. Outperforms the strongest RL-based memory baseline on LoCoMo and LongMemEval, demonstrating that co-adaptive end-to-end RL is feasible for long-horizon memory management.

## Key Contributions

- Stage-Decoupled GRPO: alternates construction and retrieval optimization phases, controlling variation from the non-optimized stage within each rollout group to prevent confounded gradient signals
- Event-Wise Credit Assignment (ECA): localizes sparse trajectory-level feedback to the specific memory events responsible, propagating event-level advantages to their constituent operations
- End-to-end online RL policy that jointly learns memory construction and retrieval — prior work either treated one offline or optimized them independently
- Outperforms strongest RL-based memory baseline on both LoCoMo and LongMemEval benchmarks

## Relevance

Extends the long-horizon agentic RL thread (QwenGyre, RSIPO, CORD, FOCUS, EnvSched) into the memory management domain — a qualitatively new subproblem where the agent must manage its own working context over extremely long horizons. Stage-Decoupled GRPO is a novel answer to the confounded group comparison problem that arises when jointly optimizing interdependent sub-policies, complementing ECA's credit assignment approach to the sparse reward problem in long trajectories.

## My Thoughts

<!-- Add your own notes here -->
