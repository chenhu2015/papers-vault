---
title: "Taming Extreme Tokens: Covariance-Aware GRPO with Gaussian-Kernel Advantage Reweighting"
authors: ["Cheng Wang", "Qin Liu", "Wenxuan Zhou", "Muhao Chen"]
date: 2026-05-27
arxiv_id: "2605.11538v1"
url: "http://arxiv.org/abs/2605.11538v1"
score: 0.88
topics: [GRPO, RL training, PPO, reward model]
status: unread
---

# Taming Extreme Tokens: Covariance-Aware GRPO with Gaussian-Kernel Advantage Reweighting

## Summary

Motivated by the insight that entropy changes in policy gradient are governed by the covariance between token probabilities and their advantages, this work proposes covariance-weighted GRPO that uses a Gaussian kernel to dynamically down-weight extreme token-level updates. The hyperparameter-free method reduces exploration-exploitation instability while preserving informative learning signals, improving reasoning benchmarks and stabilizing entropy throughout GRPO training.

## Key Contributions

- Theoretical grounding: entropy change = E[cov(token_probs, advantages)] in policy gradient
- Gaussian-kernel advantage reweighting that automatically suppresses extreme token updates
- Hyperparameter-free — no additional tuning required on top of standard GRPO
- Improved downstream reasoning performance and stable entropy curves vs baseline GRPO

## Relevance

Provides the theoretical foundation for per-token advantage weighting in GRPO that the Cancellation Hypothesis (May 26) approached empirically. Complements the May 26 credit assignment thread; the covariance lens gives a principled explanation for why token-level sensitivity matters.

## My Thoughts

<!-- Add your own notes here -->
