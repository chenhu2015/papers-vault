---
title: "Seeing Before Reasoning: Decoupling Perception and Reasoning for Shortcut-Resilient Multimodal On-Policy Self-Distillation"
authors: ["Sihan Wang", "Xiyao Liu", "Lianqing Liu", "Zhi Han"]
date: 2026-06-18
arxiv_id: "2606.19120"
url: "https://arxiv.org/abs/2606.19120"
score: 0.79
topics: [multimodal models, vision language models, VLM, RL training]
status: unread
---

# Seeing Before Reasoning: Decoupling Perception and Reasoning for Shortcut-Resilient Multimodal On-Policy Self-Distillation

## Summary

Multimodal on-policy self-distillation (OPSD) creates a visual shortcut: the privileged reference target guides the student's tokens primarily via text rather than the actual image content. ViGOS decouples the supervision by having the student first write a visual description (supervised by an image-only perception teacher) before reasoning (supervised by a privileged reasoning teacher on the same prefix), with a reference teacher used only for invalid rollouts to recover output format. This design preserves OPSD's efficiency benefits while eliminating the visual shortcut across vision-language, spatial grounding, and visual math benchmarks.

## Key Contributions

- Identifies the "visual shortcut" failure mode in multimodal OPSD: the privileged target's textual component dominates supervision, causing the model to ignore image content
- ViGOS two-phase student output: visual description first (image-only perception teacher), then reasoning (privileged reasoning teacher on same prefix)
- Reference teacher reserved only for invalid rollouts — prevents format collapse without introducing the shortcut
- Validated across five benchmark categories: general VL, expert reasoning, visual math, spatial grounding, visual-language-prior

## Relevance

Directly addresses the cross-modal interference problem from a distillation angle: AT-RL (Jun 14) handled it via token-level credit attribution (~15% high-anchor tokens), the factorized reward paper (Jun 17) handled it via per-modality reward segments, and ViGOS handles it via teacher decoupling at the supervision level — three orthogonal solutions to the same underlying problem of modality interference in multimodal RL/distillation.

## My Thoughts

<!-- Add your own notes here -->
