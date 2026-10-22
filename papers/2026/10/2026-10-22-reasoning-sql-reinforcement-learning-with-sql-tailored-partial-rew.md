---
title: "Reasoning-SQL: Reinforcement Learning with SQL Tailored Partial Rewards for Reasoning-Enhanced Text-to-SQL"
authors: ["Mohammadreza Pourreza", "Shayan Talaei", "Ruoxi Sun", "Xingchen Wan", "Hailong Li", "Azalia Mirhoseini", "Amin Saberi", "Sercan O. Arik"]
date: 2026-10-22
arxiv_id: "2503.23157v2"
url: "http://arxiv.org/abs/2503.23157v2"
score: 0.74
topics: [GRPO, reinforcement learning, reward model, RL training]
status: unread
---

# Reasoning-SQL: Reinforcement Learning with SQL Tailored Partial Rewards for Reasoning-Enhanced Text-to-SQL

## Summary

Reasoning-SQL applies GRPO to Text-to-SQL by decomposing the reward into four partial signals — schema-linking accuracy, AI feedback, n-gram similarity, and syntax validity — explicitly targeting reward sparsity in multi-subtask structured generation. RL-only training with these partial rewards outperforms SFT, and a 14B model beats o3-mini (+4%) and Gemini-1.5-Pro-002 (+3%) on BIRD. The partial reward decomposition scheme is a generalizable contribution to the step-credit / structured-reward literature.

## Key Contributions

- Four-component partial reward decomposition for Text-to-SQL addressing reward sparsity: schema-linking, AI feedback, n-gram similarity, syntax check
- RL-only GRPO training outperforms SFT on structured generation without handcrafted reasoning paths
- 14B model surpasses o3-mini and Gemini-1.5-Pro-002 on BIRD benchmark
- Demonstrates that domain-specific reward decomposition can unlock reasoning capability without inductive bias from handcrafted CoT

## Relevance

Adds a domain-specific instantiation to the step-credit cluster: the four partial rewards (each targeting a distinct subtask of Text-to-SQL) demonstrate the same principle as CALIPER's adaptive utility estimation — decompose the sparse terminal reward into intermediate signals aligned with the problem's structure. The SQL-tailored design is domain-specific, but the reward decomposition pattern (correctness + structural + format + syntax) directly parallels R-Search's multi-component reward.

## My Thoughts

<!-- Add your own notes here -->
