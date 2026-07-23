---
title: "GFlowRL: Scaling Distribution-Matching RL to Large Language Models"
authors: ["Xiaodong Liu", "Michael Xu", "Jack W. Stokes", "Paul Smolensky", "Doug Burger", "Jianfeng Gao"]
date: 2026-07-15
arxiv_id: "2607.13394"
url: "https://arxiv.org/abs/2607.13394"
score: 0.83
topics: [agentic RL, RL training, RLHF, RLAIF, reward model]
status: unread
---

# GFlowRL: Scaling Distribution-Matching RL to Large Language Models

## Summary

GFlowRL replaces the learned prompt-conditional partition function in GFlowNet-style RL with an in-batch Monte Carlo estimate, removing a major source of gradient instability as model size and rollout horizon grow. Two stabilizers—importance-sampling correction for rollout/trainer drift and asymmetric flow-gap clipping for outlier residuals—enable stable training across dense and MoE architectures up to 235B parameters. GFlowRL reaches a Codeforces rating of 2048 at 14B (within 25 Elo of o3-mini) and achieves state-of-the-art adversarial attack success rates on AdvBench/HarmBench, outperforming prior GFlowNet methods that diverge at scale.

## Key Contributions

- Replaces the auxiliary prompt-conditional partition function (the main scaling bottleneck in prior GFlowNet RL) with an in-batch Monte Carlo estimate requiring no additional network or memory overhead
- Importance-sampling correction handles rollout/trainer drift when the sampling policy diverges from the trainer distribution
- Asymmetric flow-gap clipping suppresses outlier residuals without discarding gradient signal, analogous to DISPO's asymmetric IS clipping for correct/incorrect rollouts
- Scales stably to 235B MoE, where prior FlowRL diverges; first GFlowNet RL method to succeed on both dense and sparse architectures

## Relevance

GFlowRL introduces distribution-matching RL (reward-distribution matching rather than reward maximization) as a scalable alternative to PPO/GRPO, directly extending the RL training thread (RLHF, RLAIF, GRPO failure diagnostics). The diversity-encouraging objective addresses the mode collapse failure mode identified in DEPT's self-play thread and the headroom principle from the GRPO web agent failure analysis—tasks where sampling rarely outperforms greedy may benefit from GFlowNets' inherent diversity pressure rather than reward-maximizing RL.

## My Thoughts

<!-- Add your own notes here -->
