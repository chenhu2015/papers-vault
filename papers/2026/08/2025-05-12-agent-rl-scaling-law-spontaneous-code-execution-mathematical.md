---
title: "Agent RL Scaling Law: Agent RL with Spontaneous Code Execution for Mathematical Problem Solving"
authors: ["Xinji Mai", "Haotian Xu", "Zhong-Zhi Li", "Xing W", "Weinong Wang", "Jian Hu", "Yingying Zhang", "Wenqiang Zhang"]
date: 2025-05-12
arxiv_id: "2505.07773"
url: "https://arxiv.org/abs/2505.07773"
score: 0.72
topics: [agentic RL, tool use, RL training]
status: unread
---

# Agent RL Scaling Law: Agent RL with Spontaneous Code Execution for Mathematical Problem Solving

## Summary

ZeroTIR trains base LLMs from scratch to spontaneously generate and execute Python code for math reasoning using only binary outcome rewards — no supervised tool-use examples — and establishes that code execution frequency, response length, and task accuracy all increase with strong positive correlation as RL training steps increase. This scaling law suggests tool-use emergence is quantifiably driven by compute invested in RL, not by imitation initialization. ZeroTIR significantly surpasses non-tool RL baselines on challenging math benchmarks with a decoupled code execution environment.

## Key Contributions

- Zero-shot tool-use emergence from RL alone: no SFT examples of code use required, just outcome rewards
- Empirical scaling law: code execution frequency, response length, and task accuracy all increase predictably with RL training compute
- Decoupled execution environment enabling async code evaluation during RL rollouts
- Validates across standard RL algorithms and frameworks (not algorithm-specific)

## Relevance

Complements the tool-use RL thread in the vault (EvolveVLA Aug 20 — on-the-fly tool use via RL; MAPO Aug 26 — description-alignment reward for VLM tool invocation) but from the emergence angle: where those papers assume some tool-use capability exists and improve it, ZeroTIR asks how tool-use emerges from zero under RL and finds a quantifiable scaling relationship. The scaling law finding also connects to "Does RL Expand the Capability Boundary?" (Aug 16) which asks a related question about capability emergence under RL more broadly.

## My Thoughts

<!-- Add your own notes here -->
