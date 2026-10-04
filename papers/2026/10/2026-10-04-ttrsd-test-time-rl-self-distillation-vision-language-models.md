---
title: "TTRSD: Test-Time Reinforcement Learning with Self-Distillation for Vision-Language Models"
authors: ["Shuning Wang", "Zhiheng Wu", "Xun Zhou", "Chongyang Cui", "Chen Jia", "Bowen Liu", "Chuanjie Li", "Xiang Chen", "Yi Yang", "Yumeng Zhang", "Wenjie Huang"]
date: 2026-10-04
arxiv_id: "2609.33414"
url: "https://arxiv.org/abs/2609.33414"
score: 0.78
topics: [VLM, multimodal models, vision-language, RL training, RLAIF]
status: unread
---

# TTRSD: Test-Time Reinforcement Learning with Self-Distillation for Vision-Language Models

## Summary

TTRSD enables test-time adaptation of VLMs from 20 unlabeled samples by combining multi-view answer-level self-distillation (aggregating teacher predictions across original, cropped, and downsampled image views as the reward signal) with visual contrastive token selection (comparing log-probs under original vs. visually-ablated inputs to restrict policy gradient updates to perceptually sensitive token positions). The method separates update direction (group-relative advantages) from update position (visual sensitivity) without requiring ground-truth labels, external verifiers, or a separate teacher model. TTRSD raises InternVL3-2B's MMMU accuracy from 35.79% to 49.32% (+13.53%) across seven benchmarks.

## Key Contributions

- Multi-view self-distillation as the reward signal: aggregates predictions across original, cropped, and downsampled views; no ground-truth labels needed
- Visual contrastive token selection: compares log-probs under original vs. ablated image (holding textual prefix fixed) to identify perceptually sensitive positions
- Separation of update direction (group-relative advantages) from update position (visual sensitivity) — a principled decomposition new to the VLM RL literature
- 20-sample adaptation with cross-dataset generalization across seven benchmarks and three VLM architectures

## Relevance

TTRSD's visual contrastive token selection shares the core intuition with TPAE (pivotal tokens via visual-dependency + entropy) but arrives via a different mechanism: log-prob comparison under visual ablation rather than within-correct-rollout statistics. At the training paradigm level, it connects to the no-gold-labels reward thread (CCS, cross-attention RL, RFPO, TPAE) — all avoiding external labels via model-internal signals. The test-time framing (20 unlabeled samples) is new to this cluster and raises the question of whether training-time credit methods like TPAE can also be adapted to low-data test-time settings.

## My Thoughts

<!-- Add your own notes here -->
