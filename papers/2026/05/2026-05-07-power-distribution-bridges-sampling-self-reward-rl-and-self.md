---
title: "Power Distribution Bridges Sampling, Self-Reward RL, and Self-Distillation"
authors: ["Akiyoshi Tomihari", "Issei Sato"]
date: 2026-05-06
arxiv_id: "2605.04542"
url: "https://arxiv.org/abs/2605.04542"
score: 0.82
topics: [RLHF, reward model, RL training]
status: unread
---

# Power Distribution Bridges Sampling, Self-Reward RL, and Self-Distillation

## Summary

The power distribution is shown to be the closed-form optimizer of KL-regularised RL when the model's own sequence-level log-probabilities serve as the reward, formally unifying inference-time power sampling, self-reward RL, and self-distillation under a single framework. Power self-distillation amortises power sampling into supervised training; downstream gain is governed by the covariance between true reward and self-reward under the power distribution.

## Key Contributions

- Proves the power distribution is the closed-form solution to KL-regularised RL with self-log-prob reward — unifying three seemingly distinct paradigms
- Power self-distillation: offline supervised training on teacher samples shares the same target distribution as power sampling, amortising inference cost
- Shows local (token-level) approximations cannot reproduce sequence-level power without suffix information — formalises the gap between token and sequence reward
- Experiments on reasoning tasks confirm self-reward sharpening via power distribution; true-reward gain depends on self/true-reward covariance

## Relevance

Provides a theoretical lens for understanding why self-reward RL and RLHF/RLAIF work — directly relevant to the reward model and RLHF thread. Helps explain when GRPO (which uses group log-prob advantages) can be viewed as a form of self-reward KL-regularised RL, connecting to the GRPO variants covered throughout the digest.

## My Thoughts

<!-- Add your own notes here -->
