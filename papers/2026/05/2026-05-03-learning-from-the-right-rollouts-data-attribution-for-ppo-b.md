---
title: "Learning from the Right Rollouts: Data Attribution for PPO-based LLM Post-Training"
authors: ["Dong Shu", "Denghui Zhang", "Jessica Hullman"]
date: 2026-05-03
arxiv_id: "2604.01597v1"
url: "http://arxiv.org/abs/2604.01597v1"
score: 0.84
topics: [PPO, RL training, reward model, RLHF]
status: unread
---

# Learning from the Right Rollouts: Data Attribution for PPO-based LLM Post-Training

## Summary

Standard PPO trains on all rollouts including noisy or unfaithful reasoning episodes, which degrades LLM post-training. Influence-Guided PPO (I-PPO) computes a gradient-based influence score per episode and discards rollouts anti-aligned with a validation gradient, acting as an intrinsic early stopping mechanism. I-PPO consistently outperforms SFT and vanilla PPO baselines while reducing unfaithful chain-of-thought reasoning.

## Key Contributions

- Applies data attribution (influence functions) to the PPO rollout buffer to score individual episodes by their alignment with a validation gradient
- Filters out anti-aligned (harmful) episodes before the policy update, reducing noise in the optimization signal
- Demonstrates that this filtering acts as intrinsic early stopping, improving training efficiency
- Reduces unfaithful CoT reasoning as a direct byproduct of removing low-quality rollouts

## Relevance

This is a practical improvement to PPO post-training for LLMs, targeting the exact problem of noisy rollouts that degrades reward-following and reasoning. Complements the exploration/exploitation work seen in recent digests (HeRL, DEEP-GRPO) by attacking data quality rather than trajectory coverage.

## My Thoughts

<!-- Add your own notes here -->
