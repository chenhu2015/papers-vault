---
title: "Visual-OPSD: Cross-Modal On-Policy Self-Distillation for Efficient Unified Multimodal Reasoning"
authors: ["Pengyu Li", "Zhitao Gao", "Lingling Zhang", "Muye Huang", "Yuanming Li", "Fangzhi Xu", "Jun Liu"]
date: 2026-07-05
arxiv_id: "2606.18974"
url: "https://arxiv.org/abs/2606.18974"
score: 0.72
topics: [VLM, multimodal models, RL training, vision-language]
status: unread
---

# Visual-OPSD: Cross-Modal On-Policy Self-Distillation for Efficient Unified Multimodal Reasoning

## Summary

Visual-OPSD reuses visual thoughts (VTs) generated during SFT as privileged teacher context for on-policy KL distillation, avoiding the order-of-magnitude generation cost of new VTs during RL training rounds. Teacher and student share identical weights but differ in context (teacher sees VTs, student sees text-only); token-level JSD distillation on student rollouts transfers the generation pathway's reasoning without regenerating pixels, yielding +3.40pp improvement over the generative teacher with 14.3x speedup.

## Key Contributions

- Key finding: VT content barely changes accuracy when removed, but the generation pathway encodes reasoning beyond rendered pixels (confirmed by KL diagnostic)
- Visual-OPSD: reuse SFT-time VTs as teacher context; student rollouts provide the on-policy target — no new VT generation during RL
- Token-level JSD distillation transfers generation pathway reasoning to text-only student
- +3.40pp over generative teacher, 14.3x speedup (10.0s vs 142.8s/sample), +63.83pp on VSP

## Relevance

Visual-OPSD resolves a practical constraint that limited the VLM on-policy distillation thread: GTR-Turbo (Jul 2) and CRAFT (Jul 2) required online rollouts from the teacher during training, which is expensive for VLMs with diffusion-based visual generation. Visual-OPSD's key insight — that the generation pathway's semantic content rather than its rendered pixels is what matters for distillation — directly enables the same cross-modal on-policy signal at 14x lower cost, making the technique practical for unified multimodal model training.

## My Thoughts

<!-- Add your own notes here -->
