---
title: "DRM: Diffusion-based Reward Model With Step-wise Guidance"
authors: ["Jaxon Zhang", "Binxin Yang", "Hubery Yin", "Chen Li", "Jing Lyu"]
date: 2026-05-26
arxiv_id: "2605.25661v1"
url: "http://arxiv.org/abs/2605.25661v1"
score: 0.83
topics: [reward model, GRPO, multimodal models, RL training]
status: unread
---

# DRM: Diffusion-based Reward Model With Step-wise Guidance

## Summary

DRM introduces a diffusion model as a reward backbone for aligning generative image models, leveraging its ability to assess both final images and noisy intermediate latents at any stage of the generation process. Step-wise GRPO uses these dense per-step rewards to resolve GRPO's imprecise credit assignment problem, yielding more stable and effective alignment than outcome-only reward signals. Step-wise Sampling additionally employs DRM as a dynamic inference-time guide to evaluate multiple generation paths at each denoising step, steering toward higher-quality outputs.

## Key Contributions

- Proposes pre-trained diffusion model as reward backbone: uniquely able to evaluate final images and noisy intermediate latents at any generation stage
- Step-wise GRPO: provides dense per-step rewards that resolve GRPO's credit assignment imprecision for diffusion model alignment
- Step-wise Sampling: inference strategy using DRM as a dynamic guide to steer generation paths toward higher quality
- Significant improvements on aesthetic, preference, and compositional metrics for image generation

## Relevance

Extends the step-level credit assignment thread (DeLTA, PAIR, SRaR) to the diffusion/image generation domain and connects with the diffusion RL cluster (Precise, Linear-DPO). The Step-wise GRPO contribution is directly applicable to GRPO credit assignment problems in LLM training as well.

## My Thoughts

<!-- Add your own notes here -->
