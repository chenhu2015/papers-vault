---
title: "Forecasting How RLHF Responds to Reward-Model Edits Before Training"
authors: ["Zixiao Wang", "Duzhen Zhang", "Xingbo Du", "Dongxia Wu", "Le Song"]
date: 2026-11-02
arxiv_id: "2611.03244v2"
url: "http://arxiv.org/abs/2611.03244v2"
score: 0.80
topics: [RLHF, reward model, GRPO, RL training, RLAIF]
status: unread
---

# Forecasting How RLHF Responds to Reward-Model Edits Before Training

## Summary

Shows that a policy's behavioral response to a reward-model edit can be forecast before RL training using within-prompt covariance between the RM score change and each behavioral feature, derived from first-order KL-regularized RL theory. Validated across 54 RL runs with controlled RM edits under a fractional factorial design, the covariance predictor explains 82% of standardized feature movement direction and 66% out-of-sample for real RM upgrades, and correctly ranks edits by reward-proxy rent at step 30 (Spearman 0.94) before the ranking reverses at step 200.

## Key Contributions

- First-order theory: policy feature change ∝ within-prompt covariance between RM score change and that feature — analytically derived from KL-regularized RL
- Covariance predictor explains 82% of standardized feature direction (vs 50% for counterfactual prices), validated in 2^(4-1) factorial design across 54 RL runs
- 66% out-of-sample explanation for real RM upgrades; horizon effect: short-run rankings freeze then reverse by step 200 under both GRPO and RLOO
- Reveals reward-hacking dynamics: format features (headers, length) driven by covariance, not genuine quality improvement

## Relevance

Provides a theoretical and empirical lens for understanding reward-model effects on GRPO/RLHF training — directly relevant to the GRPO objective variants cluster and the reward hacking concern raised by RLCDR. This paper predicts which RM edits will improve alignment before spending compute on RL runs.

## My Thoughts

<!-- Add your own notes here -->
