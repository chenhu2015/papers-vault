---
title: "Linear-DPO: Linear Direct Preference Optimization for Diffusion and Flow-Matching Generative Models"
authors: ["Kesong Li", "Yixuan Xu", "Kuo-kun Tseng", "Weiyi Lu", "Kan Liu", "Tao Lan"]
date: 2026-05-25
arxiv_id: "2605.21123v1"
url: "http://arxiv.org/abs/2605.21123v1"
score: 0.74
topics: [RLHF, multimodal models, RL training, vision-language]
status: unread
---

# Linear-DPO: Linear Direct Preference Optimization for Diffusion and Flow-Matching Generative Models

## Summary

Linear-DPO derives a generalized DPO objective covering both diffusion and flow-matching models through a unified reverse-time SDE framework, identifying that the standard sigmoid utility is suboptimal for regression-based generative tasks. The proposed linear utility function combined with an EMA-updated reference model produces more stable and effective alignment than sigmoid-based DPO across SD1.5, SDXL, and SD3-Medium on text-to-image generation. This extends preference optimization methods like RLHF/DPO to the multimodal generative domain in a principled way.

## Key Contributions

- Derives a generalized DPO objective unifying diffusion and flow-matching via reverse-time SDE framework
- Identifies via gradient analysis that sigmoid utility is suboptimal for regression-based generation tasks
- Proposes linear utility function as drop-in replacement for sigmoid; adds EMA-updated reference model for stability
- Validated on three major architectures: SD1.5, SDXL (diffusion) and SD3-Medium (flow-matching)

## Relevance

Directly relevant to the RLHF and multimodal models keywords in the interest profile — brings DPO/preference optimization into the generative image model domain. Paired well with Precise (also found today) in establishing the RL-for-generative-models search angle as a productive new vein.

## My Thoughts

<!-- Add your own notes here -->
