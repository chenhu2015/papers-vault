---
title: "Reward Modeling from Natural Language Human Feedback"
authors: ["Zongqi Wang", "Rui Wang", "Yuchuan Wu", "Yiyao Yu", "Pinyi Zhang", "Shaoning Sun", "Yujiu Yang", "Yongbin Li"]
date: 2026-06-07
arxiv_id: "2601.07349v3"
url: "http://arxiv.org/abs/2601.07349v3"
score: 0.80
topics: [RLHF, RLAIF, reward model, RL training, reinforcement learning]
status: unread
---

# Reward Modeling from Natural Language Human Feedback

## Summary

RM-NLHF demonstrates that RLVR-trained Generative Reward Models trained on binary pairwise classification are susceptible to guessing correct preference labels without sound critique, introducing noise into the reward signal. The fix uses natural language human critique as process reward signals — computing similarity between GRM-generated and human critiques rather than outcome-only binary labels — providing richer supervision that suppresses spurious successes. MetaRM extends this by learning to predict process rewards from human-critiqued data and then generalising to uncritiqued data, consistently outperforming outcome-only GRMs across multiple benchmarks.

## Key Contributions

- Diagnosis: RLVR-based GRMs trained on binary tasks can guess correct preference labels without genuine critique, creating noisy reward signals
- RM-NLHF: uses similarity between GRM-generated and human critiques as process reward signal, replacing binary outcome supervision
- MetaRM: learns to predict process rewards from critiqued data and generalises to uncritiqued data (scalability mechanism)
- Consistent outperformance of outcome-only GRMs across multiple evaluation benchmarks

## Relevance

Directly addresses the RLAIF/reward model improvement carry-forward from June 6. Pairs naturally with SAVE (June 6, on-policy RM self-improvement) — SAVE improves RM by staying in sync with policy distribution; RM-NLHF improves RM by replacing binary labels with richer natural language process signals. Together they address two orthogonal weaknesses of standard reward model training.

## My Thoughts

<!-- Add your own notes here -->
