---
title: "Difficulty-Adaptive Tree-Structured Policy Optimization for Expanding Reasoning Coverage in RLVR"
authors: ["Youngjun Yu", "Sanghwan Jang", "Hwanjo Yu"]
date: 2026-09-08
arxiv_id: "2609.08650v1"
url: "http://arxiv.org/abs/2609.08650v1"
score: 0.84
topics: [RL training, reinforcement learning, GRPO, RLHF]
status: unread
---

# Difficulty-Adaptive Tree-Structured Policy Optimization for Expanding Reasoning Coverage in RLVR

## Summary

DATPO identifies three design principles for expanding pass@k in RLVR: difficulty-adaptive rollout allocation expands coverage beyond being a mere efficiency heuristic; tree-based rollout outperforms parallel sampling in discovering correct answers; and sentence-entropy-guided forking overcomes token-level branching's localization phenomenon to maximize semantic diversity. DATPO integrates these with a sibling-diversity advantage term that explicitly promotes semantic diversity during training. Math reasoning benchmarks show DATPO outperforms baselines particularly in pass@k, which directly translates to superior test-time scaling.

## Key Contributions

- Establishes pass@k expansion as the primary goal of rollout structural design (not just efficiency)
- Difficulty-adaptive rollout: harder problems get more branches — serves exploration, not just compute allocation
- Sentence-level entropy forking: token-level entropy exhibits localization (forks cluster near punctuation/conjunctions); sentence-level avoids this and maximizes semantic diversity
- Sibling-diversity advantage term: explicit diversity reward within a tree's sibling groups

## Relevance

Direct companion to EPIG-Tree (variance decomposition → branching rules) and Belief-Shift Branching (fork placement via value pivots). DATPO addresses a third dimension: *difficulty-adaptive* budget allocation across the training corpus. Combined, these three papers form a comprehensive design space for tree-structured RLVR rollout.

## My Thoughts

<!-- Add your own notes here -->
