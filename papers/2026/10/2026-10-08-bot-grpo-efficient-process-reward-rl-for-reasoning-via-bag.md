---
title: "BoT-GRPO: Efficient Process-Reward RL for Reasoning via Bag-of-Token Aggregation"
authors: ["Yingxiang Yang", "Weihang Xiao", "Zhunxuan Wang", "Joshua Flashner"]
date: 2026-10-08
arxiv_id: "2610.09804v1"
url: "http://arxiv.org/abs/2610.09804v1"
score: 0.93
topics: [GRPO, reward model, agentic RL, RL training, PPO]
status: unread
---

# BoT-GRPO: Efficient Process-Reward RL for Reasoning via Bag-of-Token Aggregation

## Summary

BoT-GRPO extends GRPO to token-level process rewards via a length-invariant bag-of-tokens aggregation: token rewards across rollouts are weighted by inverse source-sequence length, and per-token advantages are computed relative to weighted group statistics. The algorithm is critic-free and a drop-in replacement for GRPO wherever a token-level reward model is available, reaching 1.9× faster convergence on code generation and 8.1% absolute Pass@k gains on AIME reasoning versus standard GRPO. Key practical finding: reward stability matters more than reward richness — clean, bounded, stable signals consistently accelerate learning where noisier alternatives stall.

## Key Contributions

- Length-invariant bag-of-tokens aggregation that brings token-level process rewards into GRPO without a value network
- Drop-in replacement design: works wherever GRPO is used when a token-level reward model is available
- Empirical comparison against GSPO, DAPO, PURE on both code generation and mathematical reasoning tasks
- Practical recipe: reward stability > richness for token-level RL; noisy fine-grained signals can stall rather than accelerate learning

## Relevance

Directly addresses the open question of how to make GRPO benefit from step-level process supervision — the exact integration point between the user's GRPO interest and the step-credit cluster (ASCT, GACA, AdaStep, etc.). BoT-GRPO is the first method to make this a drop-in replacement, removing the value-network cost that kept prior PRM+PPO approaches expensive.

## My Thoughts

<!-- Add your own notes here -->
