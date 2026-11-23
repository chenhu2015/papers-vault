---
title: "Gradient-Gated DPO: Stabilizing Preference Optimization in Language Models"
authors: ["Inoussa Mouiche", "Abderaouf Bahi"]
date: 2026-05-04
arxiv_id: "2605.02626"
url: "https://arxiv.org/abs/2605.02626"
score: 0.72
topics: [RLHF, reward model, RL training]
status: unread
---

# Gradient-Gated DPO: Stabilizing Preference Optimization in Language Models

## Summary

Gate-DPO identifies a DPO failure mode called the squeezing effect: when rejected responses enter low-probability valleys, continued negative updates redistribute mass away from unrelated responses via coupled softmax geometry. Gate-DPO selectively attenuates gradient contributions from low-probability rejected responses using their current probability geometry, composing with DPO, KTO, and IPO objectives; across four architectures and two preference datasets, gating reduces squeezing and improves chosen-response likelihood.

## Key Contributions

- Formal analysis of the squeezing effect: large preference margins can conceal substantial suppression of unrelated responses, misleading standard evaluation metrics
- Gradient-Gated Preference Optimization (Gate-DPO): uses current probability geometry of each rejected response to selectively attenuate its training contribution
- Objective-agnostic: composes as a wrapper on top of DPO, IPO, KTO without changing the base objective
- Mass-dynamics analysis showing gating achieves healthier probability redistribution than vanilla DPO

## Relevance

Third entry in the RLHF training dynamics thread alongside Forecasting RLHF (RM-to-policy covariance propagation) and Bradley-Terry Distortion (BT objective shifts probability mass to impossible outcomes): Gate-DPO addresses DPO's intra-training probability collapse at the rejected-response level, providing a complementary mechanism to BT-level distortion corrections.

## My Thoughts

<!-- Add your own notes here -->
