---
title: "MarsRL: Advancing Multi-Agent Reasoning System via Reinforcement Learning with Agentic Pipeline Parallelism"
authors: ["Shulin Liu", "Dong Du", "Tao Yang", "Yang Li", "Boyu Qiu"]
date: 2026-06-06
arxiv_id: "2511.11373v1"
url: "http://arxiv.org/abs/2511.11373v1"
score: 0.85
topics: [agentic RL, RL training, reinforcement learning, multimodal models]
status: unread
---

# MarsRL: Advancing Multi-Agent Reasoning System via Reinforcement Learning with Agentic Pipeline Parallelism

## Summary

MarsRL jointly trains all agents in a multi-agent reasoning system (Solver, Verifier, Corrector) using RL with agent-specific reward mechanisms, addressing the failure of prior methods to generalise cooperative reasoning to open-source models. A pipeline-inspired training schedule handles long trajectories efficiently, and the framework achieves 93.3% on AIME2025 with Qwen3-30B (up from 86.5%) and 73.8% on BeyondAIME, surpassing much larger models. The key insight is that jointly optimising all roles — not just the solver — is essential for multi-agent RL to generalise beyond closed-source systems.

## Key Contributions

- Identifies that existing multi-agent reasoning systems fail on open-source models due to insufficient critic and correction capabilities
- Introduces agent-specific reward mechanisms to mitigate reward noise across different roles (Solver, Verifier, Corrector)
- Pipeline-inspired training schedule improves efficiency for long-trajectory multi-agent RL
- Applied to Qwen3-30B-A3B: AIME2025 from 86.5% → 93.3%, BeyondAIME from 64.9% → 73.8%, surpassing Qwen3-235B

## Relevance

This resolves the 7-consecutive-day multi-agent LLM RL carry-forward (MarsRL is the clearest example of joint multi-agent RL training for LLM reasoning). The agent-specific reward decomposition directly extends prior threads on credit assignment (LangMARL, TRACER) and multi-agent GRPO (CoRe-Code, Turn-PPO).

## My Thoughts

<!-- Add your own notes here -->
