---
title: "MATCH: Model-Aware Tool Learning with Curriculum Scheduling and Hierarchically Gated Rewards"
authors: ["Shihao Liu", "Hao Yin", "Lijun Liu"]
date: 2026-09-17
arxiv_id: "2609.20082v1"
url: "https://arxiv.org/abs/2609.20082"
score: 0.85
topics: [agentic RL, RL training, tool use, GRPO]
status: unread
---

# MATCH: Model-Aware Tool Learning with Curriculum Scheduling and Hierarchically Gated Rewards

## Summary

MATCH addresses two failure modes in RL-based tool learning: fixed-threshold curricula misalign with the policy's evolving capability boundary, and additive rewards leak argument-level credit when the tool selection itself is wrong. Model-Aware Curriculum Learning (MACL) maintains reward-derived sample difficulty estimates that co-evolve with the policy, selecting boundary-adjacent and hard samples each epoch. Hierarchically gated rewards block argument-credit flow when tool selection fails, providing cleaner learning signal throughout training.

## Key Contributions

- Model-Aware Curriculum Learning (MACL): closed-loop difficulty estimation derived from per-sample reward history, selecting boundary-adjacent + top-k hard samples each epoch
- Hierarchically gated rewards: gate mechanism prevents argument-level credit from flowing when the predicted tool name is wrong — addresses reward leakage orthogonal to reward scaling
- Demonstrates that co-evolving difficulty estimates with the policy is strictly better than fixed-threshold or random sampling curricula
- Tool learning evaluation on standard LLM tool-use benchmarks with multiple backbone models

## Relevance

Directly fills the HarnessBandit curriculum gap: where HarnessBandit schedules across harnesses using learnability + transferability signals, MATCH schedules within a single task type using model-aware difficulty tracking. Together they form a two-level curriculum: which capability to train (HarnessBandit) and which instances to train on (MATCH). The gated reward mechanism is a novel complement to GRPO's group-relative normalization.

## My Thoughts

<!-- Add your own notes here -->
