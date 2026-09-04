---
title: "GAP: Graph-Based Agent Planning with Parallel Tool Use and Reinforcement Learning"
authors: ["Jiaqi Wu", "Qinlao Zhao", "Zefeng Chen", "Kai Qin", "Yifei Zhao", "Xueqian Wang", "Yuhang Yao"]
date: 2026-09-04
arxiv_id: "2510.25320v1"
url: "http://arxiv.org/abs/2510.25320v1"
score: 0.75
topics: [agentic RL, LLM agent, tool use, reinforcement learning, RLHF]
status: unread
---

# GAP: Graph-Based Agent Planning with Parallel Tool Use and Reinforcement Learning

## Summary

GAP models inter-task dependencies as explicit dependency graphs, training agents via SFT on graph-based planning traces followed by RL with a correctness-based reward on strategically sampled MHQA queries — enabling adaptive parallel and serial tool execution rather than the sequential bottleneck of ReAct. On Multi-Hop QA benchmarks GAP significantly outperforms ReAct baselines while substantially improving tool invocation efficiency through intelligent parallelization of independent sub-tasks. GAP is the first graph-structured agentic RL paper to explicitly represent which tool calls can be parallelized, adding a task-dependency-structure axis to the agentic RL design space alongside HARTS's prefix-sharing axis.

## Key Contributions

- Graph-based dependency representation: inter-task dependency graph enables explicit identification of parallelizable vs. sequential tool calls
- Two-stage training: SFT on graph-based planning traces, then RL with correctness reward on strategically selected MHQA queries where tool reasoning provides maximal value
- Significant outperformance over ReAct on Multi-Hop QA benchmarks with dramatic tool invocation efficiency gains via parallelization
- New design axis: task-dependency-structure modeling for agentic RL, complementary to HARTS's compute-efficiency axis

## Relevance

GAP adds a new axis to the agentic RL systems design space that HARTS and TeamTR left unaddressed: HARTS reduces compute redundancy within rollout trees (prefix sharing); TeamTR addresses policy staleness in multi-agent sequential fine-tuning; GAP addresses execution structure by making inter-task dependencies explicit. The combination of graph-based dependency modeling (GAP) with prefix-sharing efficiency (HARTS) and trust-region staleness control (TeamTR) could make parallel agentic RL at scale tractable — no paper studies all three together.

## My Thoughts

<!-- Add your own notes here -->
