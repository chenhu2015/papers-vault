---
title: "Ranking-Aware Calibration for Reliable Multimodal Reinforcement Learning"
authors: ["Peng Cui", "Boyao Yang", "Jun Zhu"]
date: 2026-05-16
arxiv_id: "2605.16999"
url: "http://arxiv.org/abs/2605.16999v1"
score: 0.79
topics: [VLM, multimodal, vision-language, RL training, reward model]
status: unread
---

# Ranking-Aware Calibration for Reliable Multimodal Reinforcement Learning

## Summary

Ranking-Aware Calibration (RAC) supervises VLM confidence using two signals produced by group-based RL at no extra cost: a ranking-aware group loss enforcing better rollouts receive higher confidence than worse ones within the same prompt, and a clean-corrupted pairwise loss attenuating confidence under degraded visual evidence. The ranking-aware loss also reinforces task accuracy by teaching the policy to discriminate between better and worse reasoning paths.

## Key Contributions

- Ranking-aware group loss: better rollout → higher confidence within same prompt group
- Clean-corrupted pairwise loss: confidence attenuates monotonically with visual evidence degradation
- Both signals arise from existing group-based RL at no additional labeling cost
- Improved calibration and task accuracy under corrupted inputs across 6 multimodal reasoning benchmarks

## Relevance

Fills a calibration gap in multimodal RL — existing VLM RL methods produce poorly calibrated policies; the clean-corrupted loss is especially relevant for real-world agentic deployment under noisy visual inputs.

## My Thoughts

<!-- Add your own notes here -->
