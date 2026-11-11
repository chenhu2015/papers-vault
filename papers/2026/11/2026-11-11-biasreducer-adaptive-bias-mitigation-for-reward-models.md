---
title: "BiasReducer: Adaptive Bias Mitigation for Reward Models"
authors: ["Shuang Liu", "Yongliang Miao", "Yanguang Liu", "Haoyi Xiong", "Mengnan Du"]
date: 2026-11-11
arxiv_id: "2609.32720v1"
url: "http://arxiv.org/abs/2609.32720v1"
score: 0.72
topics: [reward model, RLHF, reinforcement learning]
status: unread
---

# BiasReducer: Adaptive Bias Mitigation for Reward Models

## Summary

BiasReducer addresses reward model bias toward superficial attributes (length, confidence) using a lightweight SAE-style encoder to identify sensitive attribute directions, then edits only the linear reward head to reduce that dependence without retraining. For a new dataset it ranks attributes by influence, selects relevant ones, and applies targeted head edits. Across five reward models, BiasReducer-M improves three robustness benchmarks by 8.3–18.0 pp and reduces downstream verbosity and sycophancy.

## Key Contributions

- SAE-style encoder learns which attributes (length, confidence) the reward model is sensitive to; head-only editing avoids full retraining
- Dataset-adaptive: ranks attribute influence for each new dataset, selects only relevant edits — no fixed one-size-fits-all correction
- Lightweight: only the linear reward head is modified, no additional data or retraining cost
- Downstream transfer: reduced verbosity and sycophancy while maintaining judged output quality across five reward models

## Relevance

Connects to the VLM RL reward design thread (BayesianPRM, TACE, OVC) — where those papers focus on calibrating the PRM signal in RLVR, BiasReducer addresses calibration of outcome reward models against superficial biases. SAE-based attribute identification is a novel angle that could complement BayesianPRM's Bayesian belief approach for PRM calibration.

## My Thoughts

<!-- Add your own notes here -->
