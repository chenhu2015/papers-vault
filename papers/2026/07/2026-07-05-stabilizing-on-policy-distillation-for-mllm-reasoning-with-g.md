---
title: "Stabilizing On-Policy Distillation for MLLM Reasoning with Global Normalization"
authors: ["Dongze Hao", "Zhiwei Jin", "Chen Chen", "Haonan Lu"]
date: 2026-07-05
arxiv_id: "2606.09091"
url: "https://arxiv.org/abs/2606.09091"
score: 0.75
topics: [multimodal models, RL training, GRPO, VLM]
status: unread
---

# Stabilizing On-Policy Distillation for MLLM Reasoning with Global Normalization

## Summary

GNDPO (Globally Normalized Distillation Policy Optimization) stabilizes on-policy distillation for MLLM reasoning by transforming raw per-token KL scores into batch-level relative advantages, preventing gradient explosions from magnitude misalignment in outlier states. The approach applies the same normalization principle that GRPO uses for verifiable rewards to the distillation signal, substantially improving training robustness and downstream performance on multimodal reasoning tasks.

## Key Contributions

- Identifies gradient instability in naive token-level KL distillation as a magnitude misalignment problem in outlier states
- GNDPO: normalizes raw KL scores to batch-level relative advantages — same principle as GRPO advantage normalization applied to distillation
- Practical: prevents gradient explosions while retaining token-level supervision density
- Validated on multimodal MLLM reasoning tasks with improved robustness and downstream performance

## Relevance

GNDPO directly addresses a training stability gap in the on-policy distillation thread opened by GTR-Turbo (Jul 2) and CRAFT (Jul 2). Both papers used on-policy distillation but neither addressed the gradient instability from outlier KL states — GNDPO fills this gap. The normalization-as-stabilization insight also connects to PASS (Jul 1) which diagnosed channel contamination between dense and sparse reward signals; GNDPO shows that the same instability occurs within the dense signal itself when KL magnitudes are not normalized.

## My Thoughts

<!-- Add your own notes here -->
