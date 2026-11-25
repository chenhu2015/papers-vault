---
title: "From Rewarding What Models Say to How They Think: Attention Process Reward Model for LLM Reinforcement Learning"
authors: ["Kairong Han", "Nuanqiao Shan", "Ziyu Zhao", "Xinpeng Dong", "Zijing Hu", "Dian Jin", "Leyan Deng", "Junjian Ye", "Lujia Pan", "Fei Wu", "Kun Kuang"]
date: 2026-11-23
arxiv_id: "2611.30627v1"
url: "http://arxiv.org/abs/2611.30627v1"
score: 0.75
topics: [reward model, RLHF, PPO, RL training, GRPO]
status: unread
---

# From Rewarding What Models Say to How They Think: Attention Process Reward Model for LLM Reinforcement Learning

## Summary

APRM assigns process rewards based on internal hidden states and attention maps rather than output text, addressing "textual reward aliasing" where different reasoning paths produce identical text. With only ~46M parameters, APRM is trained on ranking and counterfactual objectives, periodically updated to handle distribution shifts, and achieves an average pass@8 gain of 2.88% when integrated with representative RL methods. This frames process reward as an internal signal about how the model reasons, not just what it outputs.

## Key Contributions

- Introduces "textual reward aliasing": different internal reasoning paths produce identical text, making text-based process rewards blind to this
- Internal process reward: hidden states + attention maps → rewards via a small 46M-parameter model
- Training: ranking objective + counterfactual objective; periodically updated during RL to handle distribution shifts
- Average 2.88% pass@8 gain across representative RL methods when APRM is integrated

## Relevance

Orthogonal to DM-PRM (which queries a frozen decision model) — APRM uses internal model activations as the reward signal. Together they represent two distinct approaches to escaping text-only process reward: one external/zero-shot (DM-PRM), one internal/trained (APRM). Relevant to the RLHF training dynamics thread.

## My Thoughts

<!-- Add your own notes here -->
