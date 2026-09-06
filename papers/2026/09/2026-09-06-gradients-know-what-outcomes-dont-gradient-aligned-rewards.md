---
title: "Gradients Know What Outcomes Don't: Unlocking Reinforcement Learning for LLM Reasoning with Gradient-Aligned Rewards"
authors: ["Leqi Zheng", "Jinbo Su", "Fang Niu", "Chaokun Wang", "Weiping Wang", "Jiajun Zhang", "Shannan Yan", "Jie Wu", "Zhaolu Kang", "Rong Fu", "Hang Zhang"]
date: 2026-09-06
arxiv_id: "2609.03342"
url: "https://arxiv.org/abs/2609.03342"
score: 0.87
topics: [GRPO, reward model, RLHF, reinforcement learning, RL training]
status: unread
---

# Gradients Know What Outcomes Don't: Unlocking Reinforcement Learning for LLM Reasoning with Gradient-Aligned Rewards

## Summary

GAR computes a dense reward for GRPO by taking the cosine similarity between a rollout's truncated gradient vector (output projection layer) and an expert-anchor gradient derived from training corpus solutions, adding less than 9% wall-clock overhead. The reward admits a closed-form multiplicative decomposition into prediction-error and activation-pattern factors, providing a mechanistic account of what the alignment signal measures. On Qwen3-4B/8B, GAR consistently outperforms GRPO on competition-level math and transfers to GPQA Diamond and MMLU-Pro without domain-specific data.

## Key Contributions

- Gradient-space dense reward: cosine similarity between rollout gradient (truncated backprop through output projection) and expert-anchor gradient from training corpus — no separate reward model, no annotation
- Closed-form multiplicative decomposition into prediction-error factor and activation-pattern factor, characterizing what the alignment signal actually measures
- <9% wall-clock overhead, compatible with standard GRPO training loops
- Cross-domain transfer: math-trained GAR generalizes to GPQA Diamond and MMLU-Pro without domain-specific data

## Relevance

GAR adds a seventh axis to the GRPO improvement design map established through Sep 05: it operates on the reward signal side (like StructReward, VIG, Q-RM) but derives signal from the gradient space rather than the output or representation space, making it orthogonal to all prior axes. The expert-anchor gradient mechanism connects directly to the Demystifying RL Post-Training finding that RL success requires the base model to already place probability on correct behaviors — GAR operationalizes this by using the gradient direction toward expert solutions as the training signal, providing a theoretically grounded alternative to verifiable-outcome rewards in domains where verification is hard.

## My Thoughts

<!-- Add your own notes here -->
