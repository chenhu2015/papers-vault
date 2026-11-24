---
title: "Heterogeneous Co-Evolution Learning for Tool-Efficient Search Agents with Zero Labels"
authors: ["Qin-Wen Luo", "Sheng Ren", "Xiang Chen", "Rui Liu", "Jun Fang", "Naiqiang Tan", "Jun Wang", "Hua Chai", "Sheng-Jun Huang"]
date: 2026-11-24
arxiv_id: "2610.39682v1"
url: "http://arxiv.org/abs/2610.39682v1"
score: 0.73
topics: [agentic RL, RL training, tool use, LLM agent]
status: unread
---

# Heterogeneous Co-Evolution Learning for Tool-Efficient Search Agents with Zero Labels

## Summary

Proposes ZEST-Search, a zero-label RL training framework for search agents that addresses two limitations of outcome-only RL: static training curricula that cannot adapt as agents improve, and treating all correct trajectories equally regardless of search efficiency. Uses heterogeneous co-evolution between a proposer (which generates training tasks around the solver's capability boundary) and a solver (which learns search-augmented reasoning via RL), with intermediate-difficulty reward for the proposer and task-local tool-aware reward for the solver that jointly optimizes task difficulty and search efficiency without labeled data.

## Key Contributions

- Heterogeneous co-evolution: proposer generates validated search tasks online via answer-first + evidence-path-guided generation
- Capability-adaptive curriculum: proposer targets the solver's evolving capability boundary rather than a fixed task distribution
- Tool-aware reward: task-local reward penalizes redundant searches while still optimizing for correctness
- Zero labels: no expert search trajectories or labeled training data required

## Relevance

Intersects tool use, agentic RL, and RL training threads; the adaptive curriculum design connects to the broader RLVR training efficiency cluster (DOT, Not All Tokens Matter). Addresses a gap in the agentic RL thread: how to train search agents when labeled agentic trajectories are unavailable.

## My Thoughts

<!-- Add your own notes here -->
