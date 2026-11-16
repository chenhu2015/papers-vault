---
title: "Diagnosing On-Policy Self-Distillation for Reasoning Language Models"
authors: ["Yang Li", "Gongle Xue", "Yuheng Yuan", "Yijia Guo", "Shizhe Zhang", "Liwen Hu", "Lei Ma"]
date: 2026-09-30
arxiv_id: "2609.39118v2"
url: "https://arxiv.org/abs/2609.39118"
score: 0.86
topics: [RL training, RLAIF, GRPO, reward model, reinforcement learning]
status: unread
---

# Diagnosing On-Policy Self-Distillation for Reasoning Language Models

## Summary

Comprehensive diagnostic study of OPSD for math reasoning across 0.6B–8B parameter models identifies that OPSD works only in narrow compatibility regimes — teacher signal is shaped by reasoning-mode alignment and the complete teacher prefix, not privileged semantics alone. Token-level analysis reveals four failure modes (ineffective length growth, stable degradation, behavioral collapse, unstable signals) that explain why OPSD outcomes range from modest gains to collapse. Concludes OPSD is a sensitive algorithm rather than a generally reliable post-training method.

## Key Contributions

- Controlled experiments spanning 0.6B–8B models isolating what determines OPSD success vs. failure
- Identifies reasoning-mode alignment (not just privileged information) as the key determinant of teacher signal quality
- Token-level analysis showing teacher signal instability and poor correlation with downstream performance
- Taxonomy of four distinct failure modes with mechanistic explanations for each

## Relevance

The diagnostic paper for the OPSD/RL+distillation cluster — provides the mechanistic explanation for why GIFT, ECOS, OASIS, and SAGE-OPD were needed. The "compatibility regime" framing connects directly to ECOS (environment-calibrated weighting selects compatible turns) and GIFT (gradient geometry filter removes incompatible teacher gradient components). The "reasoning-mode alignment" finding also explains why Echo-GRPO's idiolect alignment matters: teacher prefix must be in the student's reasoning mode to avoid the collapse regime.

## My Thoughts

<!-- Add your own notes here -->
