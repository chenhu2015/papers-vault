---
title: "PDCR: Perception-Decomposed Confidence Reward for Vision-Language Reasoning"
authors: ["Hee Suk Yoon", "Eunseop Yoon", "Ji Woo Hong", "SooHwan Eom", "Gwanhyeong Koo", "Mark Hasegawa-Johnson", "Qi Dai", "Chong Luo", "Chang D. Yoo"]
date: 2026-05-14
arxiv_id: "2605.13467"
url: "https://arxiv.org/abs/2605.13467"
score: 0.85
topics: [VLM, vision-language, multimodal, reward model, agentic RL, RLHF]
status: unread
---

# PDCR: Perception-Decomposed Confidence Reward for Vision-Language Reasoning

## Summary

Global confidence-growth rewards for VLM training cause mixture-induced signal degradation: textual reasoning steps dominate the normalisation, distorting the gradient for visual perception steps. PDCR introduces a model-internal Visual Dependence Score to cluster steps unsupervisedly into perception vs. reasoning skills, then applies intra-cluster advantage normalisation so each modality receives a correctly-scaled training signal. The method outperforms global-reward and sparse-reward baselines on vision-language reasoning benchmarks without external reward models.

## Key Contributions

- Identifies mixture-induced signal degradation as a failure mode of applying global text-RL confidence rewards to VLMs
- Visual Dependence Score: model-internal metric to quantify how much a step relies on visual information
- Unsupervised clustering separates steps into perception and reasoning skill groups
- Intra-cluster advantage normalisation corrects reward scaling for both modalities independently

## Relevance

Directly extends the VLM RL thread (SRPO, GazeVLM from May 11; Measure Twice Click Once from May 13) with a fundamentally different angle: addressing reward signal quality rather than policy architecture. Complements the process reward model interest since PDCR is essentially a self-supervised step-level reward decomposition for multimodal settings.

## My Thoughts

<!-- Add your own notes here -->
