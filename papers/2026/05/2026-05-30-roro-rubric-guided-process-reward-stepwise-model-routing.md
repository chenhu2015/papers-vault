---
title: "Rubric-Guided Process Reward for Stepwise Model Routing"
authors: ["Shenghao Ye", "Yu Guo", "Zhengheng Li", "Shuangwu Chen", "Jian Yang"]
date: 2026-05-28
arxiv_id: "2605.29310"
url: "http://arxiv.org/abs/2605.29310v1"
score: 0.79
topics: [GRPO, reward model, RL training, LLM agent]
status: unread
---

# Rubric-Guided Process Reward for Stepwise Model Routing

## Summary

RoRo trains a Rubricor to generate query-specific evaluation rubrics and a Judge to score routing trajectories under those rubrics, combining rubric-based process rewards with outcome rewards to optimize a routing policy via GRPO. On five reasoning benchmarks under both same-family and cross-family settings, RoRo consistently outperforms strong baselines with better accuracy-cost trade-offs for stepwise LLM routing.

## Key Contributions

- Rubricor + Judge alternating optimization for query-specific rubric-guided process rewards
- Process rewards from routing trajectory quality combined with outcome + cost rewards in GRPO
- Better accuracy-cost frontier than prior outcome-only routing approaches
- Cross-family generalization: works across different LLM families for the routing judge

## Relevance

Novel application of rubric-based process rewards to the model routing problem — an underexplored efficiency angle in agentic LLM systems that combines reward design with inference efficiency.

## My Thoughts

<!-- Add your own notes here -->
