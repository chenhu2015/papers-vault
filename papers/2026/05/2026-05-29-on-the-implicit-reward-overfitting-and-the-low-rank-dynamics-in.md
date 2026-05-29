---
title: "On the Implicit Reward Overfitting and the Low-rank Dynamics in RLVR"
authors: ["Hao Ye", "Jisheng Dang", "Junfeng Fang", "Bimei Wang", "Yizhou Zhang", "Ning Lv", "Wencan Zhang", "Hong Peng", "Bin Hu", "Tat-Seng Chua"]
date: 2026-05-07
arxiv_id: "2605.06523v1"
url: "http://arxiv.org/abs/2605.06523v1"
score: 0.81
topics: [RLHF, reward model, RL training, reinforcement learning, RLVR]
status: unread
---

# On the Implicit Reward Overfitting and the Low-rank Dynamics in RLVR

## Summary

Using Periodic Rank-1 Substitution, this paper reveals that RLVR capabilities concentrate in rank-1 singular components and that models can achieve strong test performance even when training rewards remain low — implicit reward overfitting to the training set. Three properties are characterized: rank-1 components hold only math reasoning (not general knowledge), RLVR optimizes a specific singular spectrum producing heavy-tailed distributions, and left singular vectors show stronger alignment tendency during training.

## Key Contributions

- Introduces Periodic Rank-1 Substitution as a diagnostic tool revealing that RLVR learning concentrates in rank-1 components
- Identifies implicit reward overfitting: satisfactory test performance despite low training rewards — a previously uncharacterized failure mode
- Shows rank-1 components encode only mathematical reasoning, not general knowledge, explaining RLVR's narrow skill transfer
- Characterizes RLVR as fundamentally optimizing a singular spectrum with heavy-tailed singular value distributions

## Relevance

Directly relevant to the RL training and reward model threads; provides a mechanistic explanation for why RLVR can overfit without apparent reward saturation, complementing the reward hacking papers (Directional Alignment May 26, LLMs Gaming Verifiers May 29).

## My Thoughts

<!-- Add your own notes here -->
