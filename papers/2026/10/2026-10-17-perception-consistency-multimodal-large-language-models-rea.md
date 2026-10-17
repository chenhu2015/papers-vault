---
title: "Perception-Consistency Multimodal Large Language Models Reasoning via Caption-Regularized Policy Optimization"
authors: ["Songjun Tu", "Qichao Zhang", "Jingbo Sun", "Yuqian Fu", "Linjing Li", "Xiangyuan Lan", "Dongmei Jiang", "Yaowei Wang", "Dongbin Zhao"]
date: 2025-09-26
arxiv_id: "2509.21854v1"
url: "http://arxiv.org/abs/2509.21854v1"
score: 0.80
topics: [vision language models, VLM, multimodal models, reinforcement learning, GRPO]
status: unread
---

# Perception-Consistency Multimodal Large Language Models Reasoning via Caption-Regularized Policy Optimization

## Summary

CapPO addresses perception-induced errors in multimodal LLMs by adding caption-based consistency regularisation during RL: responses conditioned on raw images are penalised when they diverge from responses conditioned on textual captions, anchoring reasoning to semantically faithful visual content. KL-weighted advantage estimation adaptively amplifies reinforcement signals for perceptually consistent trajectories and suppresses spurious correlations. Yields +6.0% on math-focused tasks and +2.4% on general reasoning over Qwen2.5-VL-7B.

## Key Contributions

- Caption-based consistency regularisation: minimises divergence between image-conditioned and caption-conditioned responses to anchor reasoning to faithful visual grounding
- KL-weighted advantage estimation: adaptively scales reinforcement signals, amplifying consistent trajectories and suppressing spurious ones
- +6.0% math, +2.4% general reasoning over Qwen2.5-VL-7B baseline on 10 total benchmarks
- Error analysis confirms reduced perception-related mistakes vs. baselines — not just aggregate metric improvement

## Relevance

CapPO extends the VLM RL credit/grounding thread with a cross-representation consistency approach: rather than weighting tokens by attention (VGPO) or differential entropy (MAPO), it uses a textual proxy (caption) to identify perceptually faithful trajectories. Together with VGPO and MAPO, this paper establishes a cluster of three complementary methods for anchoring RL credit to source modality signals.

## My Thoughts

<!-- Add your own notes here -->
