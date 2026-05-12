---
title: "Bringing Value Models Back: Generative Critics for Value Modeling in LLM Reinforcement Learning"
authors: ["Zikang Shan", "Han Zhong", "Liwei Wang", "Li Zhao"]
date: 2026-04-12
arxiv_id: "2604.10701v1"
url: "http://arxiv.org/abs/2604.10701v1"
score: 0.86
topics: [RL training, reward model, RLHF, PPO, agentic RL]
status: unread
---

# Bringing Value Models Back: Generative Critics for Value Modeling in LLM Reinforcement Learning

## Summary

GenAC argues that conventional discriminative scalar value models fail in LLM RL because representation complexity theory predicts value functions are hard to approximate via one-shot prediction, and empirically shows such critics do not scale reliably. The proposed generative actor-critic replaces scalar prediction with a chain-of-thought reasoning process before producing value estimates, combined with In-Context Conditioning that keeps the critic calibrated to the evolving actor; GenAC yields stronger credit assignment, ranking reliability, and OOD generalization than both value-based and value-free baselines.

## Key Contributions

- Theoretical motivation: representation complexity theory explains why scalar discriminative critics fail to scale in LLM RL
- Generative Critic: chain-of-thought reasoning prior to value estimate production, increasing expressiveness
- In-Context Conditioning: keeps the critic calibrated to the current actor's distribution throughout training
- Empirical improvements in credit assignment, ranking reliability, and OOD generalization over PPO (value-based) and GRPO (value-free) baselines

## Relevance

Directly advances the credit assignment thread in LLM RL. Prior digests covered step-level credit via PRMs and GRPO's group-relative advantages; GenAC revisits the classical actor-critic framework with a generative twist. Connects to the reward model and PPO interests in the profile, offering a practical alternative to GRPO-style value-free training.

## My Thoughts

<!-- Add your own notes here -->
