---
title: "Small RL Controller, Large Language Model: RL-Guided Adaptive Sampling for Test-Time Scaling"
authors: ["Runpeng Dai", "Tong Zheng", "Rui Liu", "Chengsong Huang", "Hongtu Zhu"]
date: 2026-06-03
arxiv_id: "2606.03102"
url: "https://arxiv.org/abs/2606.03102"
score: 0.73
topics: [reinforcement learning, LLM agent, agentic RL, RL training]
status: unread
---

# Small RL Controller, Large Language Model: RL-Guided Adaptive Sampling for Test-Time Scaling

## Summary

This paper formulates adaptive test-time sampling as an MDP and trains a lightweight RL controller to decide at each sampling round whether to stop or continue, jointly optimizing correctness, latency, and compute cost. The resulting policy admits a Lagrangian relaxation interpretation as constrained optimization with explicit budget constraints, and the controller is CPU-deployable using only answer statistics (no hidden states). Experiments show improved accuracy-compute tradeoffs over ASC and ESC baselines on MATH and reasoning tasks.

## Key Contributions

- MDP formulation of adaptive sampling: stop/continue decisions are sequential actions with a joint reward over correctness, latency, and cost
- Lagrangian relaxation interpretation provides theoretical grounding and enables exact budget targeting via binary search on the dual variable
- Controller uses only answer statistics (lightweight, CPU-runnable), avoiding dependency on LLM hidden states
- Bounded regret: policy regret tied to imitation error times worst-case per-instance gap

## Relevance

Connects agentic RL (training a decision-making controller) with the inference efficiency thread from AdaptR1 (June 1). The MDP formulation and Lagrangian analysis offer a clean framework reusable for other budget-constrained LLM control problems.

## My Thoughts

<!-- Add your own notes here -->
