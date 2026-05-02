---
title: "Policy Split: Incentivizing Dual-Mode Exploration in LLM Reinforcement with Dual-Mode Entropy Regularization"
authors: ["Jiashu Yao", "Heyan Huang", "Chuwei Luo", "Daiqing Wu", "Zeming Liu", "Yuhang Guo", "Yangyang Kang"]
date: 2026-04-13
arxiv_id: "2604.11510v1"
url: "http://arxiv.org/abs/2604.11510v1"
score: 0.82
topics: [RL training, GRPO]
status: unread
---

# Policy Split: Incentivizing Dual-Mode Exploration in LLM Reinforcement with Dual-Mode Entropy Regularization

## Summary

Policy Split bifurcates an LLM policy into a normal mode (optimizing task correctness) and a high-entropy mode (incentivising exploration diversity), both sharing parameters but trained with distinct objectives under dual-mode entropy regularization. The approach consistently outperforms entropy-guided RL baselines across model sizes on general and creative tasks. It directly addresses mode collapse in LLM RL training without sacrificing accuracy.

## Key Contributions

- Dual-mode paradigm: a single shared-parameter model operates in both normal and high-entropy modes activated by a prompt trigger
- Collaborative dual-mode entropy regularization with separate objectives per mode (correctness vs. exploration)
- High-entropy mode generates behaviorally distinct outputs that provide unique gradient signals for the shared policy
- Outperforms entropy-based RL baselines across multiple model sizes on general and creative reasoning tasks

## Relevance

Directly addresses the entropy collapse / mode collapse problem that emerges during GRPO and PPO training of LLMs — a known failure mode highlighted in the RAGEN-2 paper (template collapse) found yesterday. Provides a complementary fix that operates at the policy level rather than via reward shaping.

## My Thoughts

<!-- Add your own notes here -->
