---
title: "PR2: Predictive Routing Replay for MoE-Based LLM Reinforcement Learning"
authors: ["Daize Dong", "Junlin Chen", "Haolong Jia", "Jiang Liu", "Jiawei Wu", "Huanwei Di", "Jialian Wu", "Zhengzhong Liu", "Zicheng Liu", "Emad Barsoum", "Dimitris N. Metaxas", "Hongyi Wang"]
date: 2026-06-03
arxiv_id: "2606.00395"
url: "https://arxiv.org/abs/2606.00395"
score: 0.76
topics: [PPO, RL training, reinforcement learning, RLHF, LLM agent]
status: unread
---

# PR2: Predictive Routing Replay for MoE-Based LLM Reinforcement Learning

## Summary

PR2 targets router drift — a specific instability in PPO-style RL for Mixture-of-Experts LLMs where expert activation patterns diverge between rollout and training phases, producing unstable importance sampling weights. The solution augments each router with a lightweight evolution predictor that anticipates short-horizon changes; predicted routing is used during rollout to pre-activate likely future experts, and during training to replay consistent routing for stable importance estimation. Experiments confirm reduced distribution mismatch and improved RL stability across reasoning benchmarks.

## Key Contributions

- Identifies router drift as the root cause of PPO instability on MoE LLMs: rollout and training use different routing, creating large IS weight variance
- Lightweight per-router evolution predictor that learns short-horizon routing changes without changing the main model
- Two-phase fix: predictive routing during rollout (gradients reach future-active experts) + routing replay during training (stable IS weights)
- Theoretical and empirical validation showing reduced mismatch and stronger RL benchmark performance

## Relevance

Extends the training stability thread (EP-GRPO, M-GRPO, June 2) to MoE architectures specifically. Relevant as frontier models (Mixtral, DeepSeek-MoE) increasingly use MoE, making RL stability in this regime practically important.

## My Thoughts

<!-- Add your own notes here -->
