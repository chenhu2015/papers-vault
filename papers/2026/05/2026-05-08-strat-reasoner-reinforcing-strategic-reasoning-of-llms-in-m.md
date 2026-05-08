---
title: "Strat-Reasoner: Reinforcing Strategic Reasoning of LLMs in Multi-Agent Games"
authors: ["Yidong He", "Yutao Lai", "Pengxu Yang", "Jiarui Gan", "Jiexin Wang", "Yi Cai", "Mengchen Zhao"]
date: 2026-05-06
arxiv_id: "2605.04906v1"
url: "https://arxiv.org/abs/2605.04906v1"
score: 0.81
topics: [reinforcement learning, agentic RL, RL training, LLM agent, GRPO]
status: unread
---

# Strat-Reasoner: Reinforcing Strategic Reasoning of LLMs in Multi-Agent Games

## Summary

Strat-Reasoner addresses credit assignment in multi-agent LLM games via recursive reasoning, where each agent's chain-of-thought explicitly integrates other agents' reasoning processes, resolving the non-stationarity problem that defeats standard single-agent RL. A centralized CoT comparison module provides intermediate reward signals, and a group-relative RL objective (analogous to GRPO) optimises the policy, yielding 22.1% average improvement across diverse multi-agent games. The work directly extends GRPO-style RL to the multi-agent setting with a novel recursive credit assignment mechanism.

## Key Contributions

- Recursive reasoning paradigm: agent's CoT explicitly integrates other agents' strategies, breaking non-stationarity
- Centralized CoT comparison module as a proxy reward for intermediate reasoning quality
- Hybrid advantage + group-relative RL training (GRPO analogue) for multi-agent settings
- 22.1% average performance improvement across various multi-agent game benchmarks

## Relevance

Directly extends the multi-agent LLM RL thread (orchestration traces, Planner Matters, TCOD from May 6) with a GRPO-style RL approach specifically designed for strategic non-cooperative games. The group-relative RL objective links clearly to the GRPO/RLVR backbone papers throughout the digest.

## My Thoughts

<!-- Add your own notes here -->
