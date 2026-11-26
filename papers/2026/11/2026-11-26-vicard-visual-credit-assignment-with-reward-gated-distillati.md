---
title: "ViCARD: Visual Credit Assignment with Reward-Gated Distillation for Multimodal Reasoning"
authors: ["Zijian Huang", "Jiasi Chen"]
date: 2026-11-24
arxiv_id: "2611.33437"
url: "https://arxiv.org/abs/2611.33437"
score: 0.80
topics: [RLVR, multimodal models, VLM, reward model, GRPO]
status: unread
---

# ViCARD: Visual Credit Assignment with Reward-Gated Distillation for Multimodal Reasoning

## Summary

ViCARD addresses two RLVR failure modes in visual reasoning: zero learning signal when perceptual errors cause all rollouts to fail, and uniform advantage broadcast across every token. It integrates per-token visual supervision from a crop-teacher (image cropped to relevant area) gated by verified correctness, activating on-policy distillation only when the crop-teacher answer is correct. Improves fine-grained visual reasoning across model scales while retaining broad reasoning capabilities.

## Key Contributions

- Identifies two orthogonal RLVR failure modes in visual reasoning: all-fail groups (no learning signal when perceptual errors dominate) and uniform advantage (all tokens treated equally regardless of visual relevance)
- Crop-teacher: a teacher with the input image cropped to the relevant area provides per-token supervision, transferring fine-grained visual credit
- Reward-gated distillation: on-policy distillation activates only when the crop-teacher answers correctly, ensuring supervision quality
- For all-fail groups, samples an additional crop-teacher answer and uses it for distillation only on success, rescuing otherwise zero-gradient steps

## Relevance

Orthogonal to MSPO but addresses related problems: where MSPO decouples module-level credit, ViCARD addresses token-level credit within the visual reasoning trace. Together these two papers (from the same day) form a coherent picture of RLVR credit assignment failure modes in MLLMs: module-level (MSPO) and token-level (ViCARD). Both are refinements on the GRPO + visual reasoning combination surfaced throughout November.

## My Thoughts

<!-- Add your own notes here -->
