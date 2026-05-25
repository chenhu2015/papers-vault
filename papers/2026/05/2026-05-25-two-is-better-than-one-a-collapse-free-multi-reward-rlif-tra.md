---
title: "Two is better than one: A Collapse-free Multi-Reward RLIF Training Framework"
authors: ["Shourov Joarder", "Diganta Sikdar", "Ahsan Habib Akash", "Binod Bhattarai", "Prashnna Gyawali"]
date: 2026-05-25
arxiv_id: "2605.22620v1"
url: "http://arxiv.org/abs/2605.22620v1"
score: 0.80
topics: [RLAIF, reinforcement learning, reward model, RLHF]
status: unread
---

# Two is better than one: A Collapse-free Multi-Reward RLIF Training Framework

## Summary

This paper proposes a multi-reward RLIF (RL from internal feedback) framework that decomposes the training signal into an answer-level reward (cluster voting over rollouts) and a completion-level reward (token-wise self-certainty), combined via GDPO-based normalization to prevent reward-scale imbalance. KL-Cov regularization specifically targets low-entropy token distributions to suppress entropy collapse and preserve exploration across long-horizon reasoning. On math and code benchmarks, the method matches supervised RLVR performance without any external ground-truth supervision.

## Key Contributions

- Decomposes RLIF signal into two complementary components: answer-level cluster voting + completion-level token self-certainty
- GDPO-based normalization reduces reward-scale imbalance between the two reward components
- KL-Cov regularization targets low-entropy tokens specifically to prevent late-stage entropy collapse
- Demonstrates that unsupervised RLIF with complementary rewards can match supervised RLVR on math and code

## Relevance

Directly relevant to the RLAIF keyword in the interest profile — this is a concrete RLIF mechanism that avoids the need for human annotations by constructing internal reward signals. Builds on the self-refinement/self-reward RL thread from May 24 (SD-Zero, MISE) but focuses on multi-reward decomposition to prevent collapse rather than self-distillation.

## My Thoughts

<!-- Add your own notes here -->
