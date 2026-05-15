---
title: "SeRL: Self-Play Reinforcement Learning for Large Language Models with Limited Data"
authors: ["Wenkai Fang", "Shunyu Liu", "Yang Zhou", "Kongcheng Zhang", "Tongya Zheng", "Kaixuan Chen", "Mingli Song", "Dacheng Tao"]
date: 2025-05-25
arxiv_id: "2505.20347"
url: "https://arxiv.org/abs/2505.20347"
score: 0.80
topics: [agentic RL, RL training, reward model, RLAIF, reinforcement learning]
status: unread
---

# SeRL: Self-Play Reinforcement Learning for Large Language Models with Limited Data

## Summary

SeRL bootstraps RL training when both verifiable rewards and high-quality instructions are scarce, combining self-instruction (online problem generation with quality/diversity/difficulty filtering) and self-rewarding (majority-voting reward estimation) to eliminate external annotation. The two modules work iteratively: self-instruction generates additional training samples, self-rewarding provides reward signals for them, then standard RL trains the model. Extensive experiments show SeRL matches performance of models trained on large curated datasets with verifiable rewards across multiple reasoning benchmarks.

## Key Contributions

- Self-instruction module: generates additional problems online at each training step with robust filtering (quality, diversity, difficulty)
- Self-rewarding via majority voting: estimates rewards for self-generated problems without external annotations or verifiable signals
- Iterative self-play loop combining both modules with standard RL (e.g., GRPO)
- Matches high-quality verifiable-reward training performance on limited-data domains

## Relevance

Addresses a key practical bottleneck in the RLVR/GRPO thread: what to do when you lack verifiable rewards and curated data. SeRL's self-rewarding via majority voting is a direct complement to the reward model calibration angle (today's originally planned query 2), providing a lightweight alternative that avoids needing a separate reward model entirely. The self-instruction + self-rewarding loop also echoes the RLAIF thread from earlier digests.

## My Thoughts

<!-- Add your own notes here -->
