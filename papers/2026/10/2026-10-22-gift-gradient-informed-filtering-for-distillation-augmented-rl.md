---
title: "GIFT: Gradient Informed Filtering for Distillation Augmented Reasoning RL"
authors: ["Shijie Li", "Yilin Gao", "Tieyuan Chen"]
date: 2026-10-22
arxiv_id: "2610.30796"
url: "https://arxiv.org/abs/2610.30796"
score: 0.86
topics: [GRPO mechanics, agentic RL, RL training, RLHF, reward model]
status: unread
---

# GIFT: Gradient Informed Filtering for Distillation Augmented Reasoning RL

## Summary

GIFT resolves the tension between sparse RL rewards and dense distillation guidance for reasoning LLMs via token-level geometric decomposition of teacher gradients: the component parallel to the RL gradient measures first-order conflict and acts as a safety filter, while the orthogonal component captures novel directional guidance and is retained with higher weight. Combined with a progressive coverage annealing schedule that shrinks the distillation budget over training (ensuring conflicting updates are discarded first while complementary ones are retained), GIFT achieves up to 9.5% relative gains on hard mathematical reasoning benchmarks over strong RL+distillation baselines.

## Key Contributions

- Token-level geometric decomposition of distillation gradients: parallel component (conflict detector/safety filter) vs. orthogonal component (novelty/value estimator)
- Principled scoring rule to rank token-level teacher guidance by gradient geometry
- Progressive coverage annealing: shrinks distillation budget so the most conflicting updates are discarded first; pure RL at convergence
- Up to 9.5% relative gains on hard math reasoning; consistent across model scales

## Relevance

Directly addresses the core problem identified in the Echo-GRPO/BRAT thread: when does off-policy or teacher distillation conflict with on-policy RL training? GIFT provides a principled geometric answer (gradient conflict = parallel component) rather than heuristic gating. Connects to LGPO/EPIC's analysis of gradient mechanics and to BRAT's bounded-weight solution for multi-pass stability.

## My Thoughts

<!-- Add your own notes here -->
