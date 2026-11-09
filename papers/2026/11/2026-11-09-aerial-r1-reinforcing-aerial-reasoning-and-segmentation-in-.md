---
title: "Aerial-R1: Reinforcing Aerial Reasoning and Segmentation in MLLMs"
authors: ["Jisheng Dang", "Huaiyuan Peng", "Yixuan Wang", "Kun Wang", "Zhang Li", "Tat-Seng Chua"]
date: 2026-10-19
arxiv_id: "2610.33056"
url: "https://arxiv.org/abs/2610.33056"
score: 0.80
topics: [VLM, multimodal models, vision-language, GRPO, RLAIF, reward model]
status: unread
---

# Aerial-R1: Reinforcing Aerial Reasoning and Segmentation in MLLMs

## Summary

Aerial-R1 adapts GRPO-style policy optimization to non-autoregressive mask generation via H-GAWR (Hybrid-View Group Advantage-Weighted Regression), which constructs dynamic groups of high- and low-resolution views and bridges group-relative advantage estimation with advantage-weighted policy extraction. It addresses hallucination in MLLMs by enforcing consistency on clear aerial inputs and strictly penalizing hallucinations on ambiguous ones, developing an explicit refusal mechanism. Evaluated on VSAI-Ref, the first benchmark for joint aerial reasoning and hallucination robustness, it significantly outperforms SFT baselines in segmentation precision while mitigating fatal hallucinations in low-information scenarios.

## Key Contributions

- H-GAWR: novel advantage-weighted regression for non-autoregressive mask generation, extending GRPO to non-sequential generation tasks
- Explicit refusal mechanism: consistency enforcement on clear inputs + hallucination penalty on ambiguous inputs — the first principled refusal approach in MLLM policy optimization
- VSAI-Ref benchmark: first aerial MLLM benchmark jointly evaluating dense reasoning and hallucination robustness
- Extends the visual-parallel-to-CoT principle: consistency across views as the perceptual analogue of chain-of-thought in logic

## Relevance

This paper advances the VLM RL reward design thread (now 23+ entries) and directly responds to the Nov 8 "Tomorrow" query about the visual grounding reliability / reward-design boundary. RC-GRPO (Nov 8 honorable mention) introduced refusal calibration for GREC tasks; Aerial-R1 independently develops a refusal mechanism via consistency enforcement, adding a second approach to this emerging MLLM-refusal-RL subspace. H-GAWR's extension of GRPO to non-autoregressive generation is a novel method contribution beyond the VLM thread.

## My Thoughts

<!-- Add your own notes here -->
