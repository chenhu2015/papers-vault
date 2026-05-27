---
title: "Revisiting Reinforcement Learning with Verifiable Rewards from a Contrastive Perspective"
authors: ["Feng Zhang", "Xinhong Ma", "Ziqiang Dong", "Xi Leng", "Jianfei Zhao", "Xin Sun", "Yang Yang", "Guanjun Jiang"]
date: 2026-05-27
arxiv_id: "2605.12969v2"
url: "http://arxiv.org/abs/2605.12969v2"
score: 0.84
topics: [GRPO, RL training, RLVR, PPO, reward model]
status: unread
---

# Revisiting Reinforcement Learning with Verifiable Rewards from a Contrastive Perspective

## Summary

ConSPO reformulates GRPO as a contrastive sequence-level optimizer: it replaces clipped importance-ratio scores with length-normalized log-probabilities (aligning optimization with generation likelihoods) and uses a group-wise InfoNCE objective contrasting each positive rollout against negatives from the same group. A curriculum-scheduled margin drives progressive separation from coarse ordering early in training to strong separation later. Consistent improvements on math reasoning benchmarks across diverse backbone models.

## Key Contributions

- Discriminative reformulation of GRPO: identifies two structural flaws — likelihood-misaligned scoring and score-insensitive credit assignment
- Length-normalized log-probability scores replacing clipped ratio surrogates
- Group-wise InfoNCE objective enabling relative-score-aware credit among rollouts
- Curriculum-scheduled margin for progressive positive-negative separation

## Relevance

ConSPO provides a theoretical diagnosis of GRPO's credit assignment flaws that complements the Cancellation Hypothesis (May 26) and the covariance-aware GRPO (today). Together these three papers form a coherent cluster explaining and fixing GRPO's token/sequence-level credit problems.

## My Thoughts

<!-- Add your own notes here -->
