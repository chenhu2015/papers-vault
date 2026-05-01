---
title: "MM-Doc-R1: Agentic VLM for Long Document Visual QA with Similarity-based Policy Optimization"
authors: []
date: 2026-04-15
arxiv_id: "2604.13579"
url: "https://arxiv.org/abs/2604.13579"
score: 0.87
topics: [VLM, multimodal-models, GRPO, agentic-RL]
status: unread
---

# MM-Doc-R1: Agentic VLM for Long Document Visual QA with Similarity-based Policy Optimization

## Summary

Applies agentic VLM reasoning to long document visual QA, introducing Similarity-based Policy Optimization (SPO) which fixes GRPO's baseline bias in multi-turn RL by weighting similar trajectories more carefully. Achieves +10.4% on MMLongbench-Doc and outperforms standard GRPO by 5-6%.

## Key Contributions

- Similarity-based Policy Optimization (SPO) as a drop-in improvement over GRPO
- Fixes baseline bias in GRPO's advantage estimation for multi-turn RL
- +10.4% improvement on MMLongbench-Doc benchmark
- 5-6% gain over standard GRPO baseline

## Relevance

Directly relevant to both GRPO and multimodal/VLM threads. SPO's fix for GRPO baseline bias is applicable beyond document QA — worth reading alongside DIVA-GRPO for a broader picture of GRPO variant improvements.

## My Thoughts

<!-- Add your own notes here -->
