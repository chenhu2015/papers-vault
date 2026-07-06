---
title: "Sentence-level Reward Model can Generalize Better for Aligning LLM from Human Preference"
authors: ["Wenjie Qiu", "Yi-Chen Li", "Xuqin Zhang", "Tianyi Zhang", "Yihang Zhang", "Zongzhang Zhang", "Yang Yu"]
date: 2025-03-01
arxiv_id: "2503.04793v4"
url: "http://arxiv.org/abs/2503.04793v4"
score: 0.75
topics: [RLHF, reward model, RL training, PPO]
status: unread
---

# Sentence-level Reward Model can Generalize Better for Aligning LLM from Human Preference

## Summary

This paper proposes an intermediate-grained reward model that operates at the sentence level by segmenting responses into sentences, applying differential operations to reward outputs at sentence boundary positions, and aggregating to a response-level score via a novel attention mechanism — all trained with the Bradley-Terry objective. This sentence-level granularity occupies the gap between coarse response-level reward models (typical RLHF) and fine-grained token-level credit signals (AT-RL, TAPO), outperforming response-level reward by 2.7% on RewardBench and surpassing all baselines on AlpacaEval.

## Key Contributions

- Sentence-level reward assignment via differential operations on reward outputs at segment boundaries — extracting per-sentence credit without explicit sentence-level supervision labels
- Novel attention aggregation mechanism to combine sentence-level scores into a response-level scalar compatible with Bradley-Terry preference training
- +2.7% over response-level reward models on RewardBench; state-of-the-art on AlpacaEval across all baselines
- The intermediate granularity improves generalization relative to both coarser (response) and finer (token) reward models

## Relevance

This fills an underexplored granularity slot in the reward model hierarchy from the interest profile: the credit assignment thread in the vault has covered token-level credit (AT-RL, TAPO), role-typed segment credit (TRIAGE), and trajectory-level credit (DRE), but sentence-level preference reward — the RLHF-side analog of process supervision — has been absent. The differential boundary approach is structurally similar to how process reward models extract step-level credit from verifiable intermediate states, now applied to preference alignment rather than RL-with-verification.

## My Thoughts

<!-- Add your own notes here -->
