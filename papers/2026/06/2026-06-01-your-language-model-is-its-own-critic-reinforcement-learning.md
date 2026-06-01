---
title: "Your Language Model is Its Own Critic: Reinforcement Learning with Value Estimation from Actor's Internal States"
authors: ["Yunho Choi", "Jongwon Lim", "Woojin Ahn", "Minjae Oh", "Jeonghoon Shim", "Yohan Jo"]
date: 2026-06-01
arxiv_id: "2605.07579"
url: "https://arxiv.org/abs/2605.07579"
score: 0.88
topics: [reward model, PPO, GRPO, RLHF, LLM agent]
status: unread
---

# Your Language Model is Its Own Critic: Reinforcement Learning with Value Estimation from Actor's Internal States

## Summary

POISE uses the LLM policy's own internal hidden states and token-entropy statistics — already computed during the forward pass — to estimate a baseline value for policy gradients, eliminating the need for PPO's full-scale critic model or GRPO's multi-rollout group mean. A cross-rollout construction ensures gradient unbiasedness despite trajectory-conditioned features. On Qwen3-4B and DeepSeek-R1-Distill-Qwen-1.5B across math benchmarks, POISE matches DAPO while using less compute, performing on par with a separate LLM-scale value model.

## Key Contributions

- Lightweight probe trained on hidden states of prompt + generated trajectory to predict expected verifiable reward, eliminating separate critic or multi-rollout requirements
- Cross-rollout construction: predicts each rollout's value from an independent rollout's internal states to preserve gradient unbiasedness
- Enables higher prompt diversity per compute budget by requiring only a single rollout for value estimation
- Matches DAPO performance while reducing compute overhead and eliminating zero-advantage prompt detection sampling

## Relevance

This directly addresses a core efficiency challenge in LLM RL: PPO requires a full-scale critic (doubling memory) and GRPO requires multiple rollouts (multiplying sampling cost). POISE's internal-state approach follows the Hista/Numca runner-up thread from the May 31 digest, and is the strongest paper found today on value estimation for LLM RL.

## My Thoughts

<!-- Add your own notes here -->
