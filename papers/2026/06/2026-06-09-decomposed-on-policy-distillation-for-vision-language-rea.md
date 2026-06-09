---
title: "Decomposed On-Policy Distillation for Vision-Language Reasoning: Steering Gradients for Visual Grounding"
authors: ["Hee Suk Yoon", "Eunseop Yoon", "Jaehyun Jang", "SooHwan Eom", "Ji Woo Hong", "Mark Hasegawa-Johnson", "Qi Dai", "Chong Luo", "Chang D. Yoo"]
date: 2026-06-09
arxiv_id: "2606.00564"
url: "https://arxiv.org/abs/2606.00564"
score: 0.77
topics: [multimodal models, vision language models, VLM, RLHF]
status: unread
---

# Decomposed On-Policy Distillation for Vision-Language Reasoning: Steering Gradients for Visual Grounding

## Summary

Standard VLM on-policy distillation loss decomposes mathematically into language prior and visual grounding components whose gradient vectors are nearly orthogonal, meaning standard optimization follows a suboptimal compromise. Visual Gradient Steering (VGS) dynamically reorients the update vector to prioritize the visual subspace, identifying visual grounding as the primary bottleneck for multimodal reasoning. VGS consistently outperforms monolithic distillation across multiple settings and complex multimodal benchmarks.

## Key Contributions

- Mathematical decomposition showing language-prior and visual-grounding gradient components are ~orthogonal in VLM distillation
- Identification of visual grounding (not language prior) as the binding constraint for multimodal reasoning
- Visual Gradient Steering (VGS): dynamic gradient reorientation toward visual subspace at training time
- Consistent gains across multiple distillation settings with minimal overhead

## Relevance

This paper is the VLM perception-reasoning asymmetry paper flagged as a runner-up (0.76) from the June 8 digest. It provides a clean theoretical explanation — gradient orthogonality — for why multimodal RL/distillation methods that optimize a combined objective under-invest in visual grounding. Directly relevant to the SenseNova-MARS and OpenWebRL threads (which both involve visual + language reward optimization), and connects to the broader question of how to structure rewards in multimodal RL.

## My Thoughts

<!-- Add your own notes here -->
