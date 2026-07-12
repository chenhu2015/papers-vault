---
title: "Putting the Value Back in RL: Better Test-Time Scaling by Unifying LLM Reasoners With Verifiers"
authors: ["Kusha Sareen", "Morgane M Moss", "Alessandro Sordoni", "Rishabh Agarwal", "Arian Hosseini"]
date: 2025-05-07
arxiv_id: "2505.04842"
url: "https://arxiv.org/abs/2505.04842"
score: 0.88
topics: [agentic RL, reward model, GRPO, RL training]
status: unread
---

# Putting the Value Back in RL: Better Test-Time Scaling by Unifying LLM Reasoners With Verifiers

## Summary

RL^V augments any value-free RL method (GRPO, Leave-one-out PPO) by jointly training the LLM as both a reasoner and a generative verifier using RL-generated data, adding verification capability without significant overhead. This co-training design enables test-time compute scaling: RL^V boosts MATH accuracy by over 20% with parallel sampling and achieves 8-32x efficient test-time compute scaling compared to the base RL method. RL^V also generalizes strongly to easy-to-hard and out-of-domain tasks, and achieves 1.2-1.6x higher performance when jointly scaling parallel and sequential compute with a long reasoning R1 model.

## Key Contributions

- Identifies that value-free RL methods (GRPO, LooPPO) discard the learned value function, blocking test-time compute scaling that relies on verification
- Joint co-training: uses RL-generated rollouts to simultaneously train the LLM as a reasoner (policy) and a generative verifier (critic), at negligible overhead
- 8-32x more compute-efficient test-time scaling than the base RL method; +20% MATH accuracy with parallel sampling
- Strong easy-to-hard and OOD generalization; 1.2-1.6x higher performance with joint parallel + sequential TTS on R1 model

## Relevance

RL^V directly addresses the key design gap between training-time RL and test-time compute scaling: GRPO-family methods abandon the value function, which this paper restores via co-training. This connects to the rollout diversity thread (T1, TA-GRPO) and adds a new axis — verification co-training — to the vault's emerging framework on training-inference synergy. The generative verifier is also the inference-time complement of PRISM's MoE discriminator (Jul 11): both separate evaluative capacity from policy capacity, but PRISM operates at training alignment while RL^V operates at inference verification.

## My Thoughts

<!-- Add your own notes here -->
