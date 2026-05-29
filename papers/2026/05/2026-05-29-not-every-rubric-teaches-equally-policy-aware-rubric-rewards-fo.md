---
title: "Not Every Rubric Teaches Equally: Policy-Aware Rubric Rewards for RLVR"
authors: ["Utkarsh Tyagi", "Xingang Guo", "MohammadHossein Rezaei", "Daniel George", "Anas Mahmoud", "Jackson Lee", "Bing Liu", "Yunzhong He"]
date: 2026-05-19
arxiv_id: "2605.20164v1"
url: "http://arxiv.org/abs/2605.20164v1"
score: 0.78
topics: [GRPO, reward model, RL training, reinforcement learning, RLVR]
status: unread
---

# Not Every Rubric Teaches Equally: Policy-Aware Rubric Rewards for RLVR

## Summary

POW3R identifies that static rubric aggregations in GRPO conflate human-assigned importance with actual training utility — many criteria are already saturated or unreachable, while discriminative criteria lack large human weights. It adapts criterion-level reward weights dynamically using rollout-level contrast to emphasize criteria that currently separate policy outputs, winning 24 of 30 comparisons and reaching the same performance plateau in 2.5–4× fewer training steps.

## Key Contributions

- Identifies criterion saturation and unreachability as a failure mode in static rubric-based GRPO rewards
- POW3R framework adapts criterion weights during training via rollout-level contrast (emphasizing criteria that currently discriminate the policy's outputs)
- Preserves human-assigned category balance as the rubric objective while adapting training-signal weights — separating evaluation target from optimization signal
- Wins 24 of 30 base-policy/metric comparisons across multimodal and text-only settings; 2.5–4× fewer steps to same plateau

## Relevance

Extends the reward design thread (DVAO May 26 multi-reward weighting, step-level rubric rewards May 19); POW3R is specifically about the mismatch between human rubric importance and current policy learnability — a practical insight for multi-criteria RLVR training.

## My Thoughts

<!-- Add your own notes here -->
