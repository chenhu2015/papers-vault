---
title: "The Surprising Effectiveness of Deleting Weights in LLM Post-Training"
authors: ["Jack Lu", "Zhenbang Yang", "Mike Lasby", "Tejas Pote", "Yani Ioannou", "Mengye Ren"]
date: 2026-11-12
arxiv_id: "2611.10866v1"
url: "https://arxiv.org/abs/2611.10866"
score: 0.79
topics: [RL training, RLHF, GRPO, agentic RL]
status: unread
---

# The Surprising Effectiveness of Deleting Weights in LLM Post-Training

## Summary

Deletion Tuning zeros fewer than 0.05% of a pretrained LLM's weights (a learned binary mask over gate projections) with no other modification, matching full fine-tuning across RLVR, SFT, and on-policy distillation at scale. Beyond compression (masks are 100–1000× smaller than full checkpoints), Deletion Tuning preserves prior-task accuracy near base level where FFT, LoRA, and random sparse tuning lose up to 5.4 points under RL, addressing catastrophic forgetting. Spectral analysis (stable rank, spectrum drift, principal-weight overlap) shows Deletion Tuning is geometrically closest to FFT among parameter-efficient methods.

## Key Contributions

- 0.05% binary gate deletion matches full fine-tuning across RLVR, SFT, and on-policy distillation — no gradient flows through the language model weights
- Masks are 100–1000× smaller than FFT checkpoints, enabling efficient storage of multiple task-specific adapters
- Prior-task accuracy preserved near base level under RL (FFT, LoRA, random sparse lose up to 5.4 points) — strongest catastrophic forgetting result in parameter-efficient RL literature to date
- Spectral analysis (stable rank, spectrum drift, principal-weight overlap) confirms geometric proximity to FFT; mechanism is distinct from LoRA (low-rank structure) and random sparsity

## Relevance

Extends the parameter-efficient RL cluster (T-Router, GrowRL): Deletion Tuning achieves the most extreme parameter efficiency yet (0.05% vs T-Router's 0.466%) while matching FFT performance, and uniquely demonstrates RL-specific catastrophic forgetting prevention. The binary gate mechanism over gate projections is architecturally different from both T-Router (addressable computation-reuse bank) and GrowRL (pathway isolation), adding a third mechanism to the cluster.

## My Thoughts

<!-- Add your own notes here -->
