---
title: "Demystifying Reinforcement Learning Post-Training of Language Models"
authors: ["Donovan Clay", "Saket Gollapudi", "Sankar Harilal", "Min Jang", "Jacob Morrison", "Sewoong Oh", "Natasha Jaques"]
date: 2026-09-03
arxiv_id: "2608.24949v2"
url: "http://arxiv.org/abs/2608.24949v2"
score: 0.75
topics: [reinforcement learning, RL training, reward model, RLHF, PPO, GRPO]
status: unread
---

# Demystifying Reinforcement Learning Post-Training of Language Models

## Summary

This paper deconstructs the RL post-training algorithm in a controlled environment, isolating how four factors shape outcomes: the base model's prior distribution, reward signal granularity, prompt distribution diversity, and model scale. Using entropy of the output distribution as a comparative lens across pretraining, SFT, and RL stages, it shows that RL success fundamentally depends on whether the base model already places sufficient probability mass on desired behaviors — linking the practical RL recipe to the classical exploration problem. It also shows that so-called 'spurious rewards' depend on the prompt distribution, not just the reward definition.

## Key Contributions

- Controlled decomposition of RL post-training: isolates base model prior, reward granularity, prompt diversity, and model scale as independent variables
- Entropy lens: uses output distribution entropy to compare how pretraining, SFT, and RL each shape model certainty
- Shows 'spurious rewards' are prompt-distribution-dependent, not a fixed property of the reward signal
- Links RL post-training success to the classical exploration problem: the base model must already assign non-negligible probability to desired behaviors

## Relevance

Provides theoretical grounding for why the full GRPO improvement stack (MaxPO + OTB + StructReward) matters: the base model prior finding explains why MaxPO's L2O centering is necessary (non-centered advantages push probability mass away from correct behaviors), and the reward granularity finding explains why StructReward's dense process rewards outperform sparse outcome rewards. The entropy lens also provides a unified framework for comparing SFT-then-RL approaches (AToD, OPDVR from Aug 29–30) with pure RL approaches — both paths shape entropy, just from different starting distributions.

## My Thoughts

<!-- Add your own notes here -->
