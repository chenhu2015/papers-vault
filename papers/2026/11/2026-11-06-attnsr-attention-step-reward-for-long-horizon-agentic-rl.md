---
title: "AttnSR: Attention Step Reward for Long-Horizon Agentic RL"
authors: ["Mengsong Wu", "Tianchen Zhou", "Zhaochen Su", "Zhenhua Liu", "Zhe Cui", "Aimin Zhou"]
date: 2026-11-05
arxiv_id: "2611.07932v1"
url: "http://arxiv.org/abs/2611.07932v1"
score: 0.87
topics: [agentic RL, RL training, LLM agent]
status: unread
---

# AttnSR: Attention Step Reward for Long-Horizon Agentic RL

## Summary

AttnSR derives step-level reward allocations by tracing backward through the policy model's attention graph during training replay, requiring no separate reward model or additional rollouts. The method estimates each earlier step's relevance to the final response and reinforces or penalizes accordingly based on the terminal step signal relative to a running baseline. On ALFWorld with Qwen2.5-7B-Instruct, AttnSR raises held-out success from 91.2% to 97.1% over PPO, while cutting environment interactions by 29.9% on ScienceWorld.

## Key Contributions

- Attention-graph backward trace to estimate step relevance without additional rollouts or reward models
- Running baseline on terminal step determines sign of intermediate step rewards (reinforce vs penalize)
- Consistent improvement over PPO across all evaluated checkpoints on ALFWorld (91.2%→97.1%)
- 29.9% reduction in environment interactions on ScienceWorld with accuracy gains at every checkpoint

## Relevance

Directly extends the step-credit cluster thread: AttnSR is a lightweight alternative to process reward models that extracts credit signal purely from the policy's own attention patterns, eliminating the annotation and inference cost of separate reward models. The approach complements ProAS (reference graph), AdaStep (variance-based shrinkage), and C3 (confidence-guided correction) — all attacking the same GRPO uniform-credit problem from different angles.

## My Thoughts

<!-- Add your own notes here -->
