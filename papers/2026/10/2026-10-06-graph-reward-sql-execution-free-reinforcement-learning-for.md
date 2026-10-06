---
title: "Graph-Reward-SQL: Execution-Free Reinforcement Learning for Text-to-SQL via Graph Matching and Stepwise Reward"
authors: ["Han Weng", "Puzhen Wu", "Longjie Cui", "Yi Zhan", "Boyi Liu", "Yuanfeng Song", "Dun Zeng", "Yingxiang Yang", "Qianru Zhang", "Dong Huang", "Xiaoming Yin", "Yang Sun", "Xing Chen"]
date: 2026-10-06
arxiv_id: "2505.12380v3"
url: "https://arxiv.org/abs/2505.12380"
score: 0.72
topics: [reinforcement learning, RL training, reward model]
status: unread
---

# Graph-Reward-SQL: Execution-Free Reinforcement Learning for Text-to-SQL via Graph Matching and Stepwise Reward

## Summary

Graph-Reward-SQL replaces execution-based and LLM-based reward models in Text-to-SQL RL with a graph-matching outcome reward (GMNScore) that avoids repeated database calls and GPU overhead. StepRTM provides stepwise supervision over CTE subqueries, encouraging functional correctness and readability. Evaluated on Spider and BIRD, consistently outperforms existing reward models while significantly reducing time and memory cost.

## Key Contributions

- GMNScore: SQL graph representation-based outcome reward model, avoiding execution latency and LLM memory overhead
- StepRTM: stepwise reward model supervising CTE (Common Table Expression) subquery decomposition
- Execution-free reward pipeline — no database calls required during RL training
- Consistent improvements on Spider and BIRD benchmarks over execution-based and LLM-judge baselines

## Relevance

Graph-Reward-SQL applies step-credit principles to the Text-to-SQL domain, where CTE subqueries provide a natural decomposition point analogous to the segment/step granularity in agentic RL. The GMNScore's execution-free design parallels the no-gold-labels reward cluster (CCS, RFPO, TPAE) but via structural graph matching rather than model-internal signals. This is a domain-specific instantiation of the broader step-credit pattern, with the SQL query graph playing the role that execution traces play in DepGPO and BoostAPR.

## My Thoughts

<!-- Add your own notes here -->
