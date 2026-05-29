---
title: "CoRe-Code: Collaborative Reinforcement Learning for Code Generation"
authors: ["Zhihao Dou", "Qinjian Zhao", "Zhongwei Wan", "Xiaoyu Xia", "Sumon Biswas"]
date: 2026-05-24
arxiv_id: "2605.24812v1"
url: "http://arxiv.org/abs/2605.24812v1"
score: 0.82
topics: [agentic RL, GRPO, LLM agent, reinforcement learning]
status: unread
---

# CoRe-Code: Collaborative Reinforcement Learning for Code Generation

## Summary

CoRe-Code introduces a Planner-Coder multi-agent paradigm for code generation enhanced by a collaboration-aware GRPO stage that enforces role specialization and inter-agent alignment. It outperforms RL-based and multi-agent baselines across multiple benchmarks with three base models, improving both accuracy and execution efficiency, and generalizes to other multi-agent frameworks (retrieval, debugging agents).

## Key Contributions

- Planner-Coder paradigm: Planner generates high-level plans, Coder executes them for code — clear role specialization avoids the coordination failures of generic MAS
- Collaboration-aware GRPO training stage aligns agent roles and incentivizes cooperative plan-code consistency
- Outperforms both RL-based methods and multi-agent systems on accuracy while also improving execution time and memory efficiency
- Modular design generalizes to retrieval and debugging agent frameworks without architecture changes

## Relevance

Connects the multi-agent LLM RL thread (May 6, 23 digests) with the code generation RL angle targeted today; GRPO applied to multi-agent role specialization is a natural extension of the collaborative RL patterns seen in earlier digests.

## My Thoughts

<!-- Add your own notes here -->
