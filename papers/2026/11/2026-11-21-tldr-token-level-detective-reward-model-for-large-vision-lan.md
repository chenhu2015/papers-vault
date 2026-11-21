---
title: "TLDR: Token-Level Detective Reward Model for Large Vision Language Models"
authors: ["Deqing Fu", "Tong Xiao", "Rui Wang", "Wang Zhu", "Pengchuan Zhang", "Guan Pang", "Robin Jia", "Lawrence Chen"]
date: 2024-10-07
arxiv_id: "2410.04734"
url: "https://arxiv.org/abs/2410.04734"
score: 0.73
topics: [reward model, multimodal models, VLM, vision-language models, RLHF]
status: unread
---

# TLDR: Token-Level Detective Reward Model for Large Vision Language Models

## Summary

TLDR introduces a Token-Level Detective Reward Model for multimodal LLMs that provides fine-grained per-token annotations rather than a single binary label per response. It trains using perturbation-based synthetic hard negatives and applies token-level likelihood optimization, enabling self-correction, hallucination evaluation, and 3× faster human annotation while significantly improving base VLM performance.

## Key Contributions

- Perturbation-based method to generate synthetic hard negatives with token-level ground-truth labels, eliminating need for manual annotation
- Token-level reward model for VLMs that implicitly optimizes token-level likelihood during fine-tuning
- Dual application: self-correction of VLM outputs at inference time, and hallucination evaluation tool
- 3× speedup on human annotation tasks; significant performance gains on base VLM models

## Relevance

Surfaces the token-level credit assignment dimension of the VLM RL training cluster opened on Nov 20 (Gaze-RL uses cross-modal geometry for credit redistribution; TLDR provides direct token-level supervision via perturbation-based detection). Unlike Gaze-RL which operates at training via reward redistribution, TLDR is a reusable reward model that can be applied both during training and at inference for self-correction.

## My Thoughts

<!-- Add your own notes here -->
