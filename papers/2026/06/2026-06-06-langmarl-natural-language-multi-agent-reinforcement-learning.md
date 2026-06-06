---
title: "LangMARL: Natural Language Multi-Agent Reinforcement Learning"
authors: ["Huaiyuan Yao", "Longchao Da", "Xiaoou Liu", "Charles Fleming", "Tianlong Chen", "Hua Wei"]
date: 2026-06-06
arxiv_id: "2604.00722v1"
url: "http://arxiv.org/abs/2604.00722v1"
score: 0.84
topics: [agentic RL, reinforcement learning, RLHF, LLM agent]
status: unread
---

# LangMARL: Natural Language Multi-Agent Reinforcement Learning

## Summary

LangMARL reformulates multi-agent credit assignment in the language space: each agent receives agent-level language credit (not just global reward), and policies improve via gradient evolution directly on natural language outputs. Task-relevant causal relations are summarised from replayed trajectories to provide dense feedback under sparse reward conditions. The approach improves sample efficiency, interpretability, and generalisation across cooperative multi-agent tasks by bringing MARL's credit-assignment machinery into the LLM policy space.

## Key Contributions

- Agent-level language credit assignment: breaks the global-outcome bottleneck that obscures per-agent causal signals
- Gradient evolution in language space: policy improvement operates directly on natural language, not latent embeddings
- Trajectory replay summarisation: extracts task-relevant causal relations for dense feedback under sparse rewards
- Demonstrates improved sample efficiency, interpretability, and generalisation across diverse cooperative multi-agent tasks

## Relevance

LangMARL directly attacks the multi-agent credit assignment problem (a recurring theme from TRACER, Turn-PPO, and BranPO) but uniquely operates in the language space rather than parameter space. The combination with trajectory replay connects to the off-policy thread (POPO, ReVal) from earlier in the digest series.

## My Thoughts

<!-- Add your own notes here -->
