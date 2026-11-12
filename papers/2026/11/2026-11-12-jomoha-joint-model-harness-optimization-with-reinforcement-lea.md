---
title: "JoMoHa: Joint Model--Harness Optimization with Reinforcement Learning"
authors: ["Xudong Wu", "Guangchen Lan", "Mingqi Yuan", "Jiayu Chen"]
date: 2026-11-12
arxiv_id: "2611.11499v1"
url: "https://arxiv.org/abs/2611.11499"
score: 0.81
topics: [agentic RL, RL training, LLM agent, tool use, GRPO]
status: unread
---

# JoMoHa: Joint Model--Harness Optimization with Reinforcement Learning

## Summary

JoMoHa is the first framework to jointly train an executable harness-generation policy and a task-execution policy through RL, addressing the progressive incompatibility that emerges when optimising either component alone. Both policies learn from the same trajectory experience, achieving recursive self-improvement; ALFWorld success reaches 97.0% and WebShop and DBBench also improve. The joint optimisation prevents the harness from becoming a bottleneck that limits further model gains, extending RLVR beyond fixed scaffolding to fully adaptive agentic environments.

## Key Contributions

- First joint RL training of harness-generation policy + task-execution policy from shared trajectories
- Empirical demonstration that naive alternating training creates progressive model-harness incompatibility leading to performance degradation
- ALFWorld 97.0% success, highest among evaluated methods; WebShop and DBBench also improve
- Recursive self-improvement: agent generates its own harness improvements rather than relying on fixed human-designed scaffolding

## Relevance

Directly extends the agentic RL + tool use thread: AutoScaffold (today) uses a frozen external teacher for scaffolds; JoMoHa makes the agent learn its own harness jointly with task execution. Together they form a mini-cluster of adaptive scaffolding/harness approaches that complement the fixed-environment RLVR literature. The 97.0% ALFWorld result and RSI framing make this among the strongest agentic RL papers in the vault.

## My Thoughts

<!-- Add your own notes here -->
