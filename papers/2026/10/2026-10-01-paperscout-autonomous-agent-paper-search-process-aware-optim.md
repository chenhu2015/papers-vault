---
title: "PaperScout: An Autonomous Agent for Academic Paper Search with Process-Aware Sequence-Level Policy Optimization"
authors: ["Tingyue Pan", "Jie Ouyang", "Mingyue Cheng", "Qingchuan Li", "Zirui Liu", "Daoyu Wang", "Mingfan Pan", "Shuo Yu", "Qi Liu", "Enhong Chen"]
date: 2026-10-01
arxiv_id: "2601.10029v3"
url: "http://arxiv.org/abs/2601.10029v3"
score: 0.72
topics: [agentic RL, RL training, LLM agent]
status: unread
---

# PaperScout: An Autonomous Agent for Academic Paper Search with Process-Aware Sequence-Level Policy Optimization

## Summary

PaperScout reformulates academic paper search as sequential decision-making, with an autonomous agent that dynamically decides when and how to invoke search and expansion tools based on accumulated retrieval context. To address the granularity mismatch between token-level RL and sequence-level agent-environment interactions, it introduces PSPO (Proximal Sequence Policy Optimization), which aligns credit assignment with interaction boundaries. On synthetic and real-world benchmarks, PaperScout outperforms both structured retrieval and standard RL baselines in recall and relevance.

## Key Contributions

- Frames information retrieval as sequential decision-making: agent decides whether/when/how to invoke tools rather than following a fixed retrieval workflow
- PSPO (Proximal Sequence Policy Optimization): aligns RL credit assignment with sequence-level agent-environment interaction granularity rather than token-level PPO
- Diagnosis of granularity mismatch: token-level optimization diverges from sequence-level interactions, causing noisy credit assignment and unstable training
- Demonstrates that adaptive tool invocation outperforms both static structured retrieval and standard RL on recall and relevance metrics

## Relevance

Connects to the InfoFlow thread (dense rewards for search agents) from a different angle: where InfoFlow uses subproblem decomposition and failure hints as process signals, PaperScout addresses the credit assignment granularity problem at the sequence level. PSPO's sequence-level credit formulation is relevant to PilotRL's progressive curriculum discussion — both grapple with how to define what counts as a "step" in multi-turn agentic RL.

## My Thoughts

<!-- Add your own notes here -->
