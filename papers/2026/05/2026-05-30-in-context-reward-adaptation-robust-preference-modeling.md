---
title: "In-Context Reward Adaptation for Robust Preference Modeling"
authors: ["Zhenyu Sun", "Zheng Xu", "Ermin Wei"]
date: 2026-05-28
arxiv_id: "2605.30323"
url: "http://arxiv.org/abs/2605.30323v1"
score: 0.82
topics: [RLHF, reward model, LLM agent]
status: unread
---

# In-Context Reward Adaptation for Robust Preference Modeling

## Summary

In-Context Reward Adaptation uses transformers' in-context learning to infer reward structure from a small set of preference demonstrations, adapting on the fly to diverse and previously unseen human preference distributions without retraining. Human response time as an auxiliary input signal eliminates asymptotic bias in the transformer architecture, enabling successful adaptation across unseen preference domains.

## Key Contributions

- Transformer-based framework infers reward structure from few preference demonstrations via in-context learning
- Addresses multi-domain preference heterogeneity without fixed-domain assumptions or retraining
- Human response time as auxiliary signal to correct asymptotic bias toward ground-truth reward
- Scalable path toward flexible human-AI alignment across unseen preference distributions

## Relevance

Directly addresses reward model OOD generalization — the 3-day carry-forward in previous digests — from an in-context learning angle rather than the distribution-shift regularization angle, offering a complementary perspective.

## My Thoughts

<!-- Add your own notes here -->
