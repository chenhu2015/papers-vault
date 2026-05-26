---
title: "Sampling for Quality: Training-Free Reward-Guided LLM Decoding via Sequential Monte Carlo"
authors: ["Jelena Markovic-Voronov", "Wenhui Zhu", "Bo Long", "Zhipeng Wang", "Suyash Gupta", "Kayhan Behdin", "Bee-Chung Chen", "Deepak Agarwal"]
date: 2026-05-26
arxiv_id: "2604.16453v1"
url: "http://arxiv.org/abs/2604.16453v1"
score: 0.76
topics: [reward model, RL training, LLM agent, GRPO]
status: unread
---

# Sampling for Quality: Training-Free Reward-Guided LLM Decoding via Sequential Monte Carlo

## Summary

This work defines a principled training-free framework for reward-guided decoding via Sequential Monte Carlo (SMC), constructing a reward-augmented target distribution over complete sequences that combines model transition probabilities with prefix-dependent reward potentials, without touching model weights. The SMC algorithm includes a prefix-only efficient variant and a lookahead variant whose intermediate targets match exact marginals of the full sequence distribution. On 7B models it improves HumanEval by up to 54.9% over base and consistently outperforms GRPO, reaching 87.8% on HumanEval and 78.4% on MATH500.

## Key Contributions

- Defines reward-augmented target distribution over complete sequences: combines model transition probabilities with prefix-dependent reward potentials
- Fully training-free: leaves model weights unchanged, gains arise purely from inference-time sampling
- Two SMC variants: prefix-only (computationally efficient) and lookahead (matches exact marginals of full distribution)
- Integrates resample-move updates with Metropolis-Hastings rejuvenation and block-wise generation; subsumes temperature sampling and power-tempered objectives
- Outperforms GRPO on code (HumanEval +54.9%) and math (MATH500 +8.8%) with 7B models

## Relevance

Offers an alternative to fine-tuning-based RL (GRPO/PPO) when model weights are frozen or annotation is unavailable, directly relevant to the reward model and RL training topics. Complements the SARL (label-free training) thread by showing label-free inference-time reward guidance also surpasses GRPO.

## My Thoughts

<!-- Add your own notes here -->
