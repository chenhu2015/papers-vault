---
title: "EP-GRPO: Entropy-Progress Aligned Group Relative Policy Optimization with Implicit Process Guidance"
authors: ["Song Yu", "Li Li", "Wenwen Zhao", "Zhisheng Yang"]
date: 2026-05-06
arxiv_id: "2605.04960v1"
url: "http://arxiv.org/abs/2605.04960v1"
score: 0.87
topics: [RL training, reinforcement learning, GRPO, PPO]
status: unread
---

# EP-GRPO: Entropy-Progress Aligned Group Relative Policy Optimization with Implicit Process Guidance

## Summary

EP-GRPO identifies and quantifies three credit assignment failures in GRPO: non-uniform token informativeness, step-level polarity misalignment that penalizes correct steps, and zero-variance collapse that erases outcome gradients. It addresses these via entropy-gated modulation to prioritize high-entropy decision pivots, implicit process signals derived from policy divergence anchored to outcome advantages, and cumulative entropy mapping for progress-aligned normalization without external reward models. Experiments on math reasoning benchmarks demonstrate superior accuracy and efficiency over GRPO and its variants.

## Key Contributions

- Systematic quantification of 3 GRPO credit assignment failure modes with empirical evidence
- Entropy-gated modulation to redirect learning signal toward high-uncertainty decision points
- Implicit process supervision from policy divergence — no external process reward model required
- Progress-aligned advantage normalization via cumulative entropy mapping that maintains gradient flow under zero reward variance

## Relevance

Directly resolves the entropy/KL training stability carry-forward from June 1 (which rate-limited out); complements the advantage degeneration thread from EchoRL (June 1) by attacking the same problem from the process-signal angle rather than the rollout-echoing angle.

## My Thoughts

<!-- Add your own notes here -->
