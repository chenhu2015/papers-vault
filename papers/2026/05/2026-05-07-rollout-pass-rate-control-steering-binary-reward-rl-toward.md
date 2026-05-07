---
title: "Rollout Pass-Rate Control: Steering Binary-Reward RL Toward Its Most Informative Regime"
authors: ["Tianshu Zhu", "Wenyu Zhang", "Xiaoying Zuo", "Lun Tian", "Haotian Zhao", "Yucheng Zeng", "Jingnan Gu", "Daxiang Dong", "Jianmin Wu", "Dawei Yin", "Dou Shen"]
date: 2026-05-06
arxiv_id: "2605.05112"
url: "https://arxiv.org/abs/2605.05112"
score: 0.88
topics: [agentic RL, RL training, GRPO]
status: unread
---

# Rollout Pass-Rate Control: Steering Binary-Reward RL Toward Its Most Informative Regime

## Summary

Pass rate at 50% is proven to maximise GRPO/RLOO advantage energy, reward entropy, and contrastive signal in binary-reward agentic RL; Prefix Sampling (PS) replays trajectory prefixes to steer skewed rollout groups toward this operating point. On SWE-bench-style agentic RL, PS delivers 2× wall-clock speedup on Qwen3-14B while improving verified peak performance from 0.273 to 0.295.

## Key Contributions

- Formally proves 50% rollout pass rate is the optimal operating point for binary-reward RL (maximises reward entropy, RLOO advantage energy, and success-failure contrastive structure)
- Prefix Sampling (PS): replays successful trajectory prefixes as head-starts for failing groups and failing prefixes as handicaps for passing groups to steer toward 50%
- Stateful agent environment support: prefix states reconstructed via replay; replayed tokens excluded from the loss so only continuations are optimised
- 2.01× end-to-end wall-clock speedup on SWE-bench-style agentic RL (Qwen3-14B); generalises to AIME 2025 math reasoning

## Relevance

Directly addresses the core GRPO/agentic RL training pipeline the user follows — provides a principled analysis of why reward-signal efficiency collapses and a practical fix that doesn't require changing the reward model. Extends the thread from AEM (entropy modulation for multi-turn RL) and ResRL (gradient projection for negative samples) with an orthogonal angle: rollout batch composition rather than gradient weighting.

## My Thoughts

<!-- Add your own notes here -->
