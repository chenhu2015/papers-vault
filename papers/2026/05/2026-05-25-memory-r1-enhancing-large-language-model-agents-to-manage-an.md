---
title: "Memory-R1: Enhancing Large Language Model Agents to Manage and Utilize Memories via Reinforcement Learning"
authors: ["Sikuan Yan", "Xiufeng Yang", "Zuchao Huang", "Ercong Nie", "Zifeng Ding", "Zonggen Li", "Xiaowen Ma", "Jinhe Bi", "Kristian Kersting", "Jeff Z. Pan", "Hinrich Schütze", "Volker Tresp", "Yunpu Ma"]
date: 2026-05-25
arxiv_id: "2508.19828v5"
url: "http://arxiv.org/abs/2508.19828v5"
score: 0.83
topics: [agentic RL, RL training, LLM agent, GRPO, PPO]
status: unread
---

# Memory-R1: Enhancing Large Language Model Agents to Manage and Utilize Memories via Reinforcement Learning

## Summary

Memory-R1 trains two cooperative LLM agents — a Memory Manager (learns ADD/UPDATE/DELETE/NOOP operations on an external memory bank) and an Answer Agent (pre-selects and reasons over relevant memory entries) — using outcome-driven RL with PPO and GRPO. With only 152 training QA pairs, the framework outperforms strong baselines across LoCoMo, MSC, and LongMemEval benchmarks at 3B–14B model scales, demonstrating that RL can teach LLMs to actively manage external memory with minimal supervision.

## Key Contributions

- Two-agent RL system: Memory Manager learns structured memory operations (ADD/UPDATE/DELETE/NOOP); Answer Agent learns to pre-select relevant memory entries before reasoning
- Outcome-driven RL training using both PPO and GRPO with only 152 training QA pairs
- Adaptive memory management that generalizes across diverse question types and three benchmarks (LoCoMo, MSC, LongMemEval)
- Demonstrates scalability from 3B to 14B model sizes without architecture changes

## Relevance

This paper directly advances the agentic RL and LLM agent threads of the interest profile — specifically, applying GRPO/PPO to teach agents to actively manage external state (memory) rather than just reason over context. Followed up on the Memory-R2 runner-up thread from May 24 (LoGo-GRPO for memory agents).

## My Thoughts

<!-- Add your own notes here -->
