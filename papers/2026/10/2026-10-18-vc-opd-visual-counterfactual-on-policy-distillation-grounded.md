---
title: "VC-OPD: Visual Counterfactual On-Policy Distillation for Grounded Vision-Language Reasoning"
authors: ["Jiahe Feng"]
date: 2026-10-10
arxiv_id: "2610.14939v1"
url: "http://arxiv.org/abs/2610.14939v1"
score: 0.83
topics: [VLM RL credit assignment, on-policy distillation, multimodal models, vision-language models, GRPO]
status: unread
---

# VC-OPD: Visual Counterfactual On-Policy Distillation for Grounded Vision-Language Reasoning

## Summary

VC-OPD extends on-policy distillation (OPD) for VLM reasoning by using counterfactual visual evidence—replacing instance-specific image tokens with corrupted versions—to estimate token-level visual dependence and reweight the distillation loss toward grounding-critical tokens. The key mechanism compares teacher distributions under original vs. corrupted images, applies mass-preserving normalization to stabilize update scales, and follows a teacher-supervised warm start to reduce noisy rollouts before the counterfactual phase. This directly addresses the standard OPD failure mode of equally weighting template phrases and visually irrelevant tokens, achieving stronger performance on VQA, science reasoning, and hallucination benchmarks.

## Key Contributions

- Counterfactual image corruption (replacing instance-specific evidence) as a probe to identify visually-grounded tokens at inference time
- Original–counterfactual teacher distribution gap as a soft token-level weight signal for distillation loss
- Mass-preserving normalization to prevent unstable response-level update scales from skewed weight distributions
- Teacher-supervised warm start phase to stabilize response formats before counterfactual distillation

## Relevance

Directly extends the VLM RL credit assignment thread (14 entries): VC-OPD provides a fifth mechanism for token-level credit—counterfactual visual dependence estimation—complementing (a) value-difference (LVRL), (b) likelihood-differential (OWLET), (c) claim-decomposition (SPLIT-RL), and (d) attention-grounded re-weighting (VGPO/MAPO/CapPO). Connects the Oct 15–17 distillation thread (Dr. OPD, PTD-PO) with the credit assignment thread via counterfactual visual probing.

## My Thoughts

<!-- Add your own notes here -->
