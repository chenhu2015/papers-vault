---
title: "LUT: Latent Utility Training for Visual Reasoning"
authors: ["Jiaxuan Kang", "Siyu Chen", "Mingda Li"]
date: 2026-09-06
arxiv_id: "2608.00743"
url: "https://arxiv.org/abs/2608.00743"
score: 0.76
topics: [VLM, vision-language, multimodal models, GRPO, reinforcement learning, RL training]
status: unread
---

# LUT: Latent Utility Training for Visual Reasoning

## Summary

LUT trains latent visual reasoning in VLMs by explicitly optimizing for latent utility rather than representational shape: trajectory-level Utility-Aware Latent Distillation SFT selects latent trajectories by information gain and distills via curriculum learning, while step-level Latent Attribution Policy Optimization uses answer-to-latent attribution to differentially weight latent steps during RL without requiring costly intermediate supervision. Outperforms latent reasoning baselines across perception-intensive benchmarks at lower annotation cost, converging the NC-GRPO latent-space thread with the CSR causal-attribution paradigm.

## Key Contributions

- Utility-Aware Latent Distillation SFT: selects latent trajectories by information gain and distills via curriculum learning — no bounding-box or sketch annotation required
- Latent Attribution Policy Optimization: answer-to-latent attribution differentially weights latent steps during RL, operationalizing causal necessity in the latent space
- Two-level utility framework (trajectory and step) that mirrors OTB's token-level heterogeneity insight but applied to latent reasoning steps
- Outperforms prior latent reasoning baselines on perception-intensive VQA benchmarks at lower annotation cost

## Relevance

LUT converges two threads from the Sep digest sequence: NC-GRPO's insight that injecting Gaussian noise into the hidden layer diversifies rollouts, and CSR's insight that penalizing causally unnecessary reasoning steps improves faithfulness. LUT unifies these by using attribution to identify which latent steps actually causally determine the output, then differentially optimizing those steps in RL — essentially "causal step-necessity training in latent space." The information-gain trajectory selection (SFT stage) also echoes GAR's gradient-space alignment: both use internal model signals (gradient direction vs. information gain) to identify high-value training examples without external annotation.

## My Thoughts

<!-- Add your own notes here -->
