---
title: "Cooperative Coevolution for Resource-Constrained Agentic LLM Post-Training"
authors: ["Zhiyuan Wang", "Shengcai Liu", "Jiahao Wu", "Ning Lu", "Hui Ouyang", "Shaofeng Zhang", "Haoze Lv", "Ke Tang"]
date: 2026-10-29
arxiv_id: "2608.02391v1"
url: "http://arxiv.org/abs/2608.02391v1"
score: 0.73
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# Cooperative Coevolution for Resource-Constrained Agentic LLM Post-Training

## Summary

CoPES (Cooperative Parameter-subspace Evolution Strategy) decomposes the full parameter space into lower-dimensional subspaces and searches cooperatively to train tool-using LLM agents without backpropagation. Under the same GPU-hour budget as full-parameter GRPO, CoPES recovers 92% of GRPO's accuracy gain while requiring less than one-eighth the GPU memory. Consistently outperforms standard ES and LoRA-GRPO across five math and QA benchmarks.

## Key Contributions

- Parameter-space decomposition into cooperatively-searched lower-dimensional subspaces (bypasses exponential ES complexity)
- Memory requirement < 1/8 of full-parameter GRPO while recovering 92% of accuracy gain within same GPU-hour budget
- Backpropagation-free full-parameter training — enables post-training on devices that cannot fit GRPO gradients
- Strong pass@k performance across 5 benchmarks vs standard ES and LoRA-GRPO

## Relevance

Fills a gap in the rollout efficiency / training-cost cluster: rather than reducing rollout count or rollout generation cost, CoPES eliminates the gradient-computation bottleneck entirely via evolution strategies. Relevant to the resource-constrained agentic RL thread alongside LLMZero and FSPO; adds cooperative coevolution as a third approach to memory-efficient agentic post-training.

## My Thoughts

<!-- Add your own notes here -->
