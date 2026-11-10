---
title: "T-Router: Learning Thalamic Routing for Reasoning with Parameter-Efficient Reinforcement Learning"
authors: ["Liuxian Ma", "Jiale Dai", "Jiaqi Li", "Lu Mi"]
date: 2026-09-30
arxiv_id: "2609.39109v1"
url: "https://arxiv.org/abs/2609.39109"
score: 0.73
topics: [reinforcement learning, RL training, GRPO, agentic RL]
status: unread
---

# T-Router: Learning Thalamic Routing for Reasoning with Parameter-Efficient Reinforcement Learning

## Summary

T-Router introduces a parameter-efficient RL interface allocating only 0.466% of backbone parameters via a compressed addressable bank of block changes and a depth-recurrent controller for context-dependent routing, while keeping the backbone frozen. Trained with correctness rewards, T-Router achieves 83.64 MathAvg on an 8.95B backbone versus 73.79 for full-parameter GRPO, exceeding LoRA (77.28) on matched parameter budget, and extends to tool-mediated agentic reasoning.

## Key Contributions

- Compressed addressable bank: preserves block changes in a compact, selectively readable store; computation reuse rather than weight updates
- Depth-recurrent controller: selects which prior-block contributions are used by each receiving layer and their relative influence
- 0.466% parameter budget outperforms full GRPO: 83.64 vs 73.79 MathAvg (8.95B backbone, 3 eval rounds), exceeds LoRA at matched budget
- Extends to tool-mediated reasoning: separate search training extends the same interface to agentic tool use

## Relevance

Directly relevant to the RL training efficiency thread and GrowRL-adjacent structural approaches. T-Router's addressable computation-reuse bank is a different mechanism from GrowRL's explicit pathway isolation — where GrowRL adds new structural pathways per domain, T-Router learns to selectively reuse existing computations. Both are parameter-efficient alternatives to full-parameter GRPO, now forming a small cluster of structural/parameter-efficient RL approaches.

## My Thoughts

<!-- Add your own notes here -->
