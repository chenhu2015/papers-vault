---
title: "GDSD: Reinforcement Learning as Guided Denoiser Self-Distillation for Diffusion Language Models"
authors: ["Xiaohang Tang", "Keyue Jiang", "Che Liu", "Qifang Zhao", "Xiaoxiao Xu", "Sangwoong Yoon", "Ilija Bogunovic"]
date: 2026-05-28
arxiv_id: "2605.29398"
url: "http://arxiv.org/abs/2605.29398v1"
score: 0.78
topics: [RL training, reward model, LLM agent]
status: unread
---

# GDSD: Reinforcement Learning as Guided Denoiser Self-Distillation for Diffusion Language Models

## Summary

GDSD directly distills diffusion LLM denoisers from an advantage-guided self-teacher (the closed-form KL-regularized RL optimum) via a normalization-free objective matching, bypassing the training-inference mismatch (TIM) bias introduced by ELBO-based RL methods that use randomly-masked sequences as likelihood surrogates. On LLaDA-8B and Dream-7B across planning, math, and coding benchmarks, GDSD consistently outperforms ELBO-based SOTA with up to +19.6% test-accuracy improvements and more stable training reward dynamics.

## Key Contributions

- Advantage-guided self-teacher derived from closed-form KL-regularized RL optimum
- Normalization-free distillation objective eliminates training-inference mismatch bias
- Recent ELBO-based methods identified as pathological instances of different distillation divergences
- Up to +19.6% accuracy gain over SOTA ELBO-based methods on LLaDA-8B and Dream-7B

## Relevance

Extends the diffusion model RL thread (Precise from May 25, Linear-DPO) specifically to diffusion LLMs (discrete token generation), which is distinct from image generation diffusion RL — a novel and underexplored territory.

## My Thoughts

<!-- Add your own notes here -->
