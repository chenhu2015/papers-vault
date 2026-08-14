---
title: "Self-Boosting Vision-Language Models with Noisy Student On-Policy Self-Distillation"
authors: ["Shuai Wang", "Daoan Zhang", "Zhe Tang", "Hao Cheng", "Jiaheng Wei"]
date: 2026-07-25
arxiv_id: "2607.23125v2"
url: "http://arxiv.org/abs/2607.23125v2"
score: 0.73
topics: [vision language models, multimodal models, VLM, RL training]
status: unread
---

# Self-Boosting Vision-Language Models with Noisy Student On-Policy Self-Distillation

## Summary

NOPD (Noisy Student On-Policy Self-Distillation) enables VLM self-improvement without any external model, ground-truth labels, or verifiable rewards, using only the model's own predictions as supervision. The core insight is that prediction discrepancies between clean and corrupted inputs form a natural self-supervision signal: the student learns from corrupted inputs while the same model's clean-input predictions serve as token-level targets. On Geometry3K, NOPD improves Qwen2.5-VL-7B by 20 points with only 2.1K samples, and generalizes out-of-distribution with +7.4 points on MathVista.

## Key Contributions

- **Self-supervision without external resources**: no external teacher model, no ground-truth annotations, no verifiable reward signals required — the VLM bootstraps from its own clean-input predictions
- **Clean/noisy discrepancy signal**: corrupted inputs (noisy student) are learned against the model's own clean-input predictions, using prediction divergence between input conditions as the supervision source
- Matches and outperforms RL approaches and external-model distillation on five visual reasoning tasks
- 20-point improvement on Geometry3K (2.1K samples) and +7.4 on MathVista out-of-distribution; generalizes across 3 models on 12 benchmarks

## Relevance

NOPD connects to the SSOPD intra-group self-distillation thread from Aug 13: both avoid external teachers, but use different self-supervision sources. SSOPD uses within-group correct/wrong contrast (outcome-conditioned, no input corruption); NOPD uses clean/noisy input discrepancy (input-conditioned, no group rollout structure). Together they define the space of external-teacher-free supervision sources: (1) within-rollout group contrast by outcome (SSOPD), (2) within-sample contrast by input corruption (NOPD). Gap: no paper combines both signals.

## My Thoughts

<!-- Add your own notes here -->
