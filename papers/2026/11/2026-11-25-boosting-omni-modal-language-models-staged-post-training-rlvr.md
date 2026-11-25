---
title: "Boosting Omni-Modal Language Models: Staged Post-Training with Visually Debiased Evaluation"
authors: ["Che Liu", "Lichao Ma", "Xiangyu Tony Zhang", "Yuxin Zhang", "Haoyang Zhang", "Xuerui Yang", "Fei Tian"]
date: 2026-05-12
arxiv_id: "2605.12034v2"
url: "http://arxiv.org/abs/2605.12034v2"
score: 0.80
topics: [multimodal models, vision language models, RLVR, GRPO, VLM]
status: unread
---

# Boosting Omni-Modal Language Models: Staged Post-Training with Visually Debiased Evaluation

## Summary

OmniBoost applies a three-stage post-training recipe (balanced bi-modal SFT → mixed-modality RLVR → SFT on self-distilled data) to Qwen2.5-Omni-3B for audio-visual-text understanding. To control for visual shortcuts inflating benchmark scores, the authors introduce OmniClean, a debiased evaluation view retaining 8,551 of 16,968 audited queries. RLVR provides the first broad improvement across modalities, and self-distillation raises the 3B model to performance comparable to Qwen3-Omni-30B-A3B-Instruct without a stronger omni-modal teacher.

## Key Contributions

- OmniClean: debiased evaluation benchmark removing visually-solvable queries from 9 omni-modal benchmarks (retains 8,551/16,968 queries)
- Three-stage post-training: bi-modal SFT → mixed-modality RLVR → self-distilled SFT; RLVR is the first stage to produce broad cross-modal gains
- 3B model matches Qwen3-Omni-30B-A3B performance on OmniClean after self-distillation
- Demonstrates that balanced bi-modal SFT alone gives uneven gains, while RLVR is the primary driver for omni-modal improvement

## Relevance

This directly addresses the deferred "Omni-modal GRPO alignment" thread from Nov 24. The paper confirms that RLVR works for omni-modal models (not just vision-only) and provides a concrete recipe: SFT warmup → RLVR for cross-modal improvement → self-distillation for final gain. The vocabulary fix (omni/unified without audio/speech) correctly routed to this paper.

## My Thoughts

<!-- Add your own notes here -->
