---
title: "GRPO-λ: Credit Assignment improves LLM Reasoning"
authors: ["Prasanna Parthasarathi", "Mathieu Reymond", "Boxing Chen", "Yufei Cui", "Sarath Chandar"]
date: 2026-07-08
arxiv_id: "2510.00194v1"
url: "https://arxiv.org/abs/2510.00194"
score: 0.85
topics: [RL training, GRPO, RLHF, reward model, agentic RL]
status: unread
---

# GRPO-λ: Credit Assignment improves LLM Reasoning

## Summary

Extends GRPO with λ-returns and eligibility traces: approximates temporal-difference credit assignment within GRPO using token-level log-probabilities applied after each sequence generation, plus a critic-free approximation of the TD error, without requiring a separate value model. Multiple weighting variations for the λ-return are introduced; all outperform standard GRPO, with 30–40% improved performance during RL training across LLaMA-3.1 and Qwen-2.5 architectures and 3+ average point improvement on AIME24, Math500, OlympiadMath, MinervaMath, and AMC at 1.5B–7B scale.

## Key Contributions

- Reformulates eligibility traces using token-level log-probabilities: each token's gradient weight reflects its discounted future reward contribution, injecting TD-style credit into the GRPO update without a critic model
- Critic-free TD error approximation: avoids value-model cost while retaining the credit sensitivity of TD(λ)
- Validates across 4 math reasoning datasets at 1.5B and 7B scale; 4.5-point improvement on 7B model
- Multiple λ-return weighting variants all improve over baseline GRPO, suggesting the eligibility trace mechanism is robust to exact weighting choice

## Relevance

GRPO-λ is the principled TD-theoretic complement to MRPO's (Jul 7) manual exponential step-position schedule: where MRPO applies a hand-designed temporal decay to penalize early-step failures more heavily, GRPO-λ derives token-level credit weights from λ-return theory, making the weighting learnable in principle and grounded in the RL literature. Together they cover the two main approaches to within-trajectory credit assignment in LLM post-training: manual schedules and TD approximations. The critic-free TD approximation via token log-probabilities is also structurally similar to EGSPO's (today) use of predictive entropy as a gradient routing signal — both papers use the model's own output distribution to differentiate gradient contributions without an external critic.

## My Thoughts

<!-- Add your own notes here -->
