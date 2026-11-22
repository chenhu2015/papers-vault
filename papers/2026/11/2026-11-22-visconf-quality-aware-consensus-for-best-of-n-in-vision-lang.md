---
title: "VisConf: Quality-Aware Consensus for Best-of-N in Vision-Language Model Reasoning"
authors: ["Muhammad Usman", "Muhammad Qasim Ayub", "Usman Ahad", "Muhammad Tahir"]
date: 2026-10-17
arxiv_id: "2610.24526"
url: "https://arxiv.org/abs/2610.24526"
score: 0.80
topics: [VLM, multimodal, vision-language, reward model]
status: unread
---

# VisConf: Quality-Aware Consensus for Best-of-N in Vision-Language Model Reasoning

## Summary

VisConf addresses a gap in Best-of-N selection for VLMs: standard frequency and confidence signals fail to account for whether a sampled rollout actually engages with the visual input. VisConf scores rollout quality by multiplicatively combining visual engagement (attention to image regions) with candidate-calibrated Self-Certainty, penalizing rollouts weak in either dimension, and aggregates via Rank-Weighted Consensus (RWC). Evaluated across MathVista, MMMU-Pro, and MMStar, VisConf consistently outperforms strong BoN baselines with the largest gains when correct trajectories are underrepresented in the candidate pool.

## Key Contributions

- Identifies distributional confidence and visual attention as complementary, individually insufficient indicators of VLM rollout quality
- VisConf score: multiplicative combination of visual engagement and candidate-calibrated Self-Certainty, penalizing rollouts weak in either
- Rank-Weighted Consensus (RWC): tuning-free aggregation rule converting within-question VisConf ranks to answer-level vote weights
- Largest gains precisely in the hard regime: when correct rollouts are present but underrepresented in the pool

## Relevance

Directly addresses the test-time scaling gap for VLMs identified in the Athena-PRM thread (Nov 21 digest). While Athena-PRM provides a PRM for step-level verification during generation, VisConf operates at the rollout selection level — orthogonal mechanism for the same test-time scaling problem. Together they represent two layers of the multimodal test-time scaling stack: step-level (Athena-PRM) and rollout-level (VisConf).

## My Thoughts

<!-- Add your own notes here -->
