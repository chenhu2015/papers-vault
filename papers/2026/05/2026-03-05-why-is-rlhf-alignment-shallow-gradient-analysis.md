---
title: "Why Is RLHF Alignment Shallow? A Gradient Analysis"
authors: ["Robin Young"]
date: 2026-03-05
arxiv_id: "2603.04851v1"
url: "http://arxiv.org/abs/2603.04851v1"
score: 0.77
topics: [RLHF, reward model, PPO]
status: unread
---

# Why Is RLHF Alignment Shallow? A Gradient Analysis

## Summary

Using a martingale decomposition of sequence-level harm, this paper proves that RLHF gradient signals vanish beyond the 'harm horizon' — positions after which the output's harmfulness is already determined — explaining why KL divergence between aligned and base models concentrates on early tokens. The work introduces per-position 'harm information' and derives a recovery-penalty objective that restores gradient signal throughout the sequence.

## Key Contributions

- Formal proof that RLHF gradient signal is zero beyond the harm horizon via martingale decomposition
- Defines "harm information" I_t per position, quantifying each position's influence on overall harm
- Shows equilibrium KL divergence tracks harm information, explaining the early-token concentration effect
- Derives a recovery-penalty objective that creates non-zero gradient at all positions

## Relevance

Provides a theoretical foundation for understanding PPO/RLHF training limitations — directly relevant to the RLHF, PPO, and reward model keywords in the interest profile. The "shallow alignment" finding also helps explain why RL-trained agents can still exhibit policy collapse at deeper steps, connecting to the step-level credit assignment work (StePPO, ProceedRL) that scored highly yesterday.

## My Thoughts

<!-- Add your own notes here -->
