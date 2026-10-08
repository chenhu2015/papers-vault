---
title: "RewardWeaver: Long-Horizon Interactive Learning for Language Agents via Self-Evolving Reward Adaptation"
authors: ["Hengbo Xiao", "Boyao Zhang", "Purui Liu", "Yuxuan Zheng"]
date: 2026-10-08
arxiv_id: "2610.10120v1"
url: "http://arxiv.org/abs/2610.10120v1"
score: 0.89
topics: [agentic RL, reward model, RL training, LLM agent, RLHF]
status: unread
---

# RewardWeaver: Long-Horizon Interactive Learning for Language Agents via Self-Evolving Reward Adaptation

## Summary

RewardWeaver introduces self-evolving reward adaptation for long-horizon language agents: after each training stage it performs outcome-grounded backward attribution on low-outcome trajectories, identifies recurrent capability bottlenecks, and dynamically selects process rewards targeting those bottlenecks for the next stage. The framework maintains a validated capability space with fixed rubric semantics to prevent drift, and expands it only when recurrent failures fall outside existing rubrics. Evaluated on SOTOPIA, Amazon HistoryPrice, and a new Sales Benchmark, it achieves SOTA across social interaction, bilateral bargaining, and domain-specific sales tasks.

## Key Contributions

- Self-evolving reward adaptation loop: policy optimization → failure attribution → process reward selection → repeat
- Validated capability space with fixed rubric semantics to prevent semantic drift between stages
- Controlled expansion procedure for rubrics when recurrent failures exceed existing capability space
- SOTA on three long-horizon interaction benchmarks (social interaction, bargaining, sales)

## Relevance

Addresses the long-horizon credit assignment problem differently from AdaStep (statistical reliability) and GACA (granularity mixing): RewardWeaver adapts *which* process rewards to apply based on current policy bottlenecks, rather than improving the credit signal itself. Orthogonal to the step-credit cluster entries — this is a meta-layer that selects which credit signal to use at each training stage.

## My Thoughts

<!-- Add your own notes here -->
