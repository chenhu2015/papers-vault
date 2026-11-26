---
title: "ARS-VLM: Visually Aligned Augmented Random Search for Vision-Language Models"
authors: ["Xiangwei Wang", "Jianyuan Lin", "Peng Wang", "Saman Halgamuge"]
date: 2026-11-24
arxiv_id: "2611.32147"
url: "https://arxiv.org/abs/2611.32147"
score: 0.75
topics: [VLM, multimodal models, GRPO, RL training]
status: unread
---

# ARS-VLM: Visually Aligned Augmented Random Search for Vision-Language Models

## Summary

ARS-VLM proposes forward-only (zeroth-order) VLM post-training via Augmented Random Search as a memory-efficient alternative to GRPO, addressing two failure modes in naive ZO methods: patch-grid overfitting and catastrophic forgetting. It extracts a contrastive visual basis from paired cross-grid views and anchors shallow visual-fusion layers with a soft subspace prior. Reaches equivalent accuracy in 7.5× fewer optimization steps vs GRPO on Qwen3-VL-8B with comparable OOD generalization using only forward passes.

## Key Contributions

- Identifies two failure modes in applying standard ES/ARS to VLMs: patch-grid overfitting (perturbations latch onto grid-specific visual token artifacts) and catastrophic forgetting (unbounded high-rank parameter drift degrades OOD tasks)
- Contrastive visual basis: bilinearly paired cross-grid views provide a shared signal for perturbation direction, suppressing grid-specific artifacts
- Soft subspace anchoring: shallow visual-fusion layers anchored with a subspace prior, freeing deep reasoning layers — no reference model needed
- 7.5× fewer optimization steps than GRPO to equivalent accuracy on Qwen3-VL-8B; 75.41% OOD accuracy vs 75.31% for full-parameter GRPO

## Relevance

Opens a new efficiency angle on VLM post-training: ZO optimization completely avoids backpropagation and optimizer states, making it relevant for resource-constrained RL training scenarios. Complements the GRPO-based papers throughout November by offering an alternative training paradigm that sidesteps several of GRPO's implementation complexities (reference model, memory overhead).

## My Thoughts

<!-- Add your own notes here -->
