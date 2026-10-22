---
title: "Latent Thinking Optimization: Your Latent Reasoning Language Model Secretly Encodes Reward Signals in Its Latent Thoughts"
authors: ["Hanwen Du", "Yuxin Dong", "Xia Ning"]
date: 2026-10-22
arxiv_id: "2509.26314v3"
url: "http://arxiv.org/abs/2509.26314v3"
score: 0.73
topics: [reward model, reinforcement learning, RL training]
status: unread
---

# Latent Thinking Optimization: Your Latent Reasoning Language Model Secretly Encodes Reward Signals in Its Latent Thoughts

## Summary

LTO introduces a Latent Reward Model (LRM) — a classifier trained on internal representations of Huginn-3.5B — that detects incorrect latent thinking patterns and provides optimization signal directly in the latent space, bypassing the need for verbal chain-of-thought. A probabilistic algorithm (LTO) uses the LRM to iteratively improve the latent thinking process, with demonstrated generalization across diverse domains. Positions latent-space reward modeling as a compute-efficient alternative to verbal RL.

## Key Contributions

- Empirical finding: latent representations from correct vs. incorrect reasoning paths are highly distinguishable, even without verbal chain-of-thought
- Latent Reward Model (LRM): a latent-space classifier that predicts answer correctness directly from hidden-state trajectories
- LTO optimization algorithm: probabilistic latent-space RL loop guided by LRM, bypassing token-level generation for the "thinking" phase
- Cross-domain generalization: LRM trained on one task transfers to others, suggesting universal latent correctness signal

## Relevance

Opens a distinct branch of the reward model thread: rather than designing better verbal process rewards (CALIPER, Reasoning-SQL, R-Search), LTO asks whether a reward model operating entirely in latent space can supervise non-verbal reasoning. Complements the diffusion LM RL thread (DiSPO, RSPO, StepRS-GRPO) conceptually — both grapple with supervising non-token-by-token generation — but LTO is the first to apply this to latent continuous representations in an AR-based model.

## My Thoughts

<!-- Add your own notes here -->
