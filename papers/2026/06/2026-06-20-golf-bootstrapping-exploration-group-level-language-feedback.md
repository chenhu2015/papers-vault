---
title: "Bootstrapping Exploration with Group-Level Natural Language Feedback in Reinforcement Learning"
authors: ["Lei Huang", "Xiang Cheng", "Chenxiao Zhao", "Guobin Shen", "Junjie Yang", "Xiaocheng Feng", "Yuxuan Gu", "Xing Yu", "Bing Qin"]
date: 2026-03-04
arxiv_id: "2603.04597v1"
url: "http://arxiv.org/abs/2603.04597v1"
score: 0.77
topics: [agentic RL, RL training, RLAIF, RLHF, LLM agent]
status: unread
---

# Bootstrapping Exploration with Group-Level Natural Language Feedback in Reinforcement Learning

## Summary

GOLF aggregates two complementary group-level feedback sources — external critiques identifying errors/fixes and intra-group alternative attempts supplying diverse failure patterns — and injects the synthesized refinements as off-policy scaffolds to guide targeted exploration in sparse-reward regions. This creates a virtuous training cycle: better rollouts yield richer feedback, richer feedback improves exploration efficiency. Achieves 2.2x sample efficiency improvement over scalar-reward-only RL on both verifiable and non-verifiable benchmarks.

## Key Contributions

- Two-source group-level feedback aggregation: external critiques + intra-group failure diversity
- Off-policy scaffold injection specifically in sparse-reward regions (targeted, not uniform)
- Joint optimization of generation and refinement within a unified RL loop
- 2.2x sample efficiency gain on verifiable and non-verifiable tasks

## Relevance

GOLF connects the ExpRL (Jun 16, hidden reference solutions as reward scaffold for RL mid-training) and ARBOR (Jun 19, rubric memory accumulating cross-query process rewards) threads with a third path to dense reward scaffolding in sparse-reward RL: language feedback aggregated from the group dynamics itself. ExpRL uses expert references, ARBOR uses accumulated rubrics, GOLF uses intra-group failure diversity — three distinct sources for the same "scaffold the sparse reward" objective. The virtuous cycle structure (rollouts → feedback → better exploration) is also structurally analogous to RODS (Jun 18, Popoviciu-guided synthesis) but operates at the feedback quality level rather than the data selection level.

## My Thoughts

<!-- Add your own notes here -->
