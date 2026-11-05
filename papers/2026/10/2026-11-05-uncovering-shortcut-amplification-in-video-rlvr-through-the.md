---
title: "Uncovering Shortcut Amplification in Video RLVR through the Lens of Perceptual Uncertainty Collapse"
authors: ["Jiafeng Liang", "Xianhao Ou", "Tao Ren", "Rongchuan Mu", "Runxuan Liu", "Dandan Tu", "Ming Liu", "See-Kiong Ng", "Bing Qin"]
date: 2026-10-27
arxiv_id: "2610.37211v1"
url: "http://arxiv.org/abs/2610.37211v1"
score: 0.82
topics: [VLM, multimodal, GRPO, RL training, reward model, vision-language, RLHF]
status: unread
---

# Uncovering Shortcut Amplification in Video RLVR through the Lens of Perceptual Uncertainty Collapse

## Summary

Video RLVR training causes perceptual uncertainty collapse: the model's answer distribution sharpens under outcome-level optimization, but the fraction of uncertainty reduction attributable to visual evidence progressively diminishes — gradient analysis shows confidence gains increasingly dominated by text-prior compression rather than visual grounding. BSPO (Bifocal Self-distillation Policy Optimization) addresses this via reasoning-sensitive token reweighting from intra-group rollout contrasts and shortcut-aware visual perturbation that penalizes predictions invariant to weakened visual evidence.

## Key Contributions

- Identifies perceptual uncertainty collapse: visual evidence contribution to uncertainty reduction decreases monotonically during RLVR training
- Gradient-direction analysis: confidence gains become increasingly misaligned with visually grounded uncertainty reduction as training progresses
- BSPO: identifies reasoning-sensitive tokens from intra-group correct/incorrect rollout contrasts, penalizes predictions invariant to weakened visual evidence
- Empirically validates that BSPO improves video reasoning performance and visual faithfulness simultaneously

## Relevance

Directly advances both the VLM RL reward design thread (a mechanistic explanation for why video RLVR produces shortcut-biased models) and the GRPO training dynamics thread (perceptual uncertainty collapse is a novel failure mode complementing the primacy bias and OOD generalization failures). The BSPO remedy is structurally similar to MIRA's deceptive augmentation (also found today) — two independent approaches to the same visual grounding problem.

## My Thoughts

<!-- Add your own notes here -->
