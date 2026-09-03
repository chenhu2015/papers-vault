---
title: "Perturb the Thought, Not the Pixels: Latent-Space Rollout Diversification for Reinforcement Learning of Vision-Language Models"
authors: ["Michael Jerge", "Joseph Pelczar", "Justin Downes"]
date: 2026-09-03
arxiv_id: "2608.21595v1"
url: "http://arxiv.org/abs/2608.21595v1"
score: 0.82
topics: [VLM, GRPO, multimodal models, vision-language, agentic RL]
status: unread
---

# Perturb the Thought, Not the Pixels: Latent-Space Rollout Diversification for Reinforcement Learning of Vision-Language Models

## Summary

NC-GRPO injects scale-calibrated Gaussian noise into the last hidden layer of the prompt-encoding pass for half of each GRPO rollout group, creating rollout branches from a displaced latent departure state rather than varying decoding temperature or pixel-space image distortion. Branches that reach the correct answer despite the displacement are reinforced over those derailed by it, converting latent sensitivity at the branch point into a clean policy-gradient signal. Applied to Qwen2.5-VL-7B on Geometry3K, NC-GRPO significantly improves OOD mathematical reasoning across five benchmarks while also improving hallucination robustness — an axis on which image-space noise perturbation regresses.

## Key Contributions

- Proposes latent-space noise injection (last hidden layer) as a rollout diversification mechanism for GRPO, replacing temperature or pixel perturbation
- Demonstrates independent stochastic diversity (not noise budget or direction) is the active ingredient, isolated via mechanism ablations
- Shows improvement on both OOD generalization and hallucination robustness simultaneously, where image-space noise achieves OOD gains at the cost of hallucination regression
- Modality-agnostic design: integrates into a standard RLVR pipeline as a ~50-line change to the inference engine

## Relevance

Directly extends the VLM/multimodal RL thread from Sep 02 (StructReward, HARTS, WM-R1): those papers modified reward signal, rollout tree architecture, and environment model respectively, while NC-GRPO adds a fourth axis — latent departure state diversification. Together these constitute a multi-axis view of where GRPO-style VLM RL can be improved: reward signal (StructReward), advantage estimator (MaxPO + OTB), rollout efficiency (HARTS), environment (WM-R1), and now rollout diversity at the latent level (NC-GRPO).

## My Thoughts

<!-- Add your own notes here -->
