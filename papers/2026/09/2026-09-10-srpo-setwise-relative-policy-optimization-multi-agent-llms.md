---
title: "SRPO: Setwise Relative Policy Optimization for Multi-Agent LLMs"
authors: ["Shengtian Yang", "Ziyu Xiong", "Yu Li", "Yewen Li", "Qingpeng Cai", "Lei Feng"]
date: 2026-09-10
arxiv_id: "2609.08452v1"
url: "https://arxiv.org/abs/2609.08452v1"
score: 0.82
topics: [GRPO, agentic RL, RL training, LLM agent]
status: unread
---

# SRPO: Setwise Relative Policy Optimization for Multi-Agent LLMs

## Summary

SRPO extends GRPO to multi-agent LLM settings by treating the active set — the minimal set of outputs consumed by one state transition — as a single joint multi-agent action. It combines member log-ratios into a cardinality-normalized set ratio, assigns one relative advantage to the set, and clips once, unifying fixed, mixed, and dynamically routed multi-agent workflows in one training interface. Experiments on mathematical reasoning and multi-turn search show the strongest macro-average results across four model scales, with stable optimization diagnostics under different event reductions and set sizes.

## Key Contributions

- **Active set as unit of action**: minimal set of outputs consumed by one state transition treated as one multi-agent action, aligning optimization unit with execution unit
- **Cardinality-normalized set ratio**: combines member log-ratios into a single ratio that is independent of set size, enabling different division-of-labor configurations
- **Single relative advantage + single clip**: one advantage and one clip operation per set, matching GRPO's structure at the set level
- **Unified interface**: handles fixed-role, mixed-role, and dynamically routed multi-agent workflows without architectural changes

## Relevance

SRPO is the natural GRPO extension for multi-agent LLM training — a gap that GRPO alone cannot fill because GRPO treats individual responses, not joint sets. Given the interest in agentic RL and multi-turn settings, SRPO provides the formal extension of the GRPO machinery (PPO/GRPO keyword match) to cooperative multi-agent pipelines, which complements SAPO/SAO's efficiency focus and TRIAL/T-STAR's credit assignment focus.

## My Thoughts

<!-- Add your own notes here -->
