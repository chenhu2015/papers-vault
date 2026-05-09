---
title: "MARTI-MARS²: Scaling Multi-Agent Self-Search via Reinforcement Learning for Code Generation"
authors: ["Shijie Wang", "Pengfei Li", "Yikun Fu", "Kaifeng Liu", "Fangyuan Li", "Yang Liu", "Xiaowei Sun", "Zonglin Li", "Siyao Zhao", "Jian Zhao", "Kai Tian", "Dong Li", "Junqi Gao", "Yutong Zhang", "Yiqun Chen", "Yuqiang Li", "Zoe Li", "Weinan Zhang", "Peng Ye", "Shuyue Hu", "Lei Bai", "Bowen Zhou", "Kaiyan Zhang", "Biqing Qi"]
date: 2026-05-09
arxiv_id: "2602.07848v1"
url: "http://arxiv.org/abs/2602.07848v1"
score: 0.79
topics: [agentic RL, reinforcement learning, LLM agent, multimodal models]
status: unread
---

# MARTI-MARS²: Scaling Multi-Agent Self-Search via Reinforcement Learning for Code Generation

## Summary

MARTI-MARS² integrates policy learning with multi-agent tree search for code generation, formulating collaborative exploration as a dynamic learnable environment that enables evolution from homogeneous multi-role to heterogeneous multi-agent training. Two collaborating 32B models achieve 77.7% on code benchmarks, outperforming GPT-5.1. The paper reveals a scaling law: transitioning from single-agent to heterogeneous multi-agent paradigms progressively increases RL performance ceilings, policy diversity, and test-time scaling capability.

## Key Contributions

- Multi-Agent Reinforced Training and Inference with Self-Search Scaling (MARTI-MARS²) framework
- Dynamic learnable environment formulating multi-agent collaborative exploration as an RL problem
- Evolution path: parameter-sharing homogeneous → heterogeneous multi-agent, each stage raising the RL performance ceiling
- MARTI-MARS²-T+ inference strategy exploiting multi-agent test-time scaling; 77.7% on code benchmarks beating GPT-5.1

## Relevance

Extends the multi-agent LLM RL thread (TCOD, Planner Matters, RecursiveMAS from May 6) to the code generation domain, with the added angle of tree search (connecting to the MCTS coverage from May 8). The heterogeneous multi-agent scaling law is a novel finding on top of the multi-agent RL literature.

## My Thoughts

<!-- Add your own notes here -->
