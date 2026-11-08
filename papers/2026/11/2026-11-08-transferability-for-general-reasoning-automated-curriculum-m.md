---
title: "Transferability for General Reasoning: An Automated Curriculum for Multi-Domain RLVR"
authors: ["Yongjin Yang", "Jiarui Liu", "Yinghui He", "Lechen Zhang", "Bernhard Schölkopf", "Zhijing Jin"]
date: 2026-06-23
arxiv_id: "2606.25178v2"
url: "https://arxiv.org/abs/2606.25178"
score: 0.82
topics: [agentic RL, RL training, GRPO, RLHF, reward model]
status: unread
---

# Transferability for General Reasoning: An Automated Curriculum for Multi-Domain RLVR

## Summary

TAC (Transfer-Aware Curriculum) is a bandit-style online curriculum for multi-domain RLVR that prioritizes domains whose gradient updates broadly benefit the rest of the training suite, combining per-domain advantages (local learnability) with projected GRPO gradient alignment (cross-domain transferability) at <1% wall-clock overhead. Unlike learnability-only curricula that over-commit to dominant domains, TAC's transferability signal prevents skill-siloing and achieves the best macro-averaged accuracy on a six-domain reasoning suite with Qwen3-1.7B and Llama3.2-3B, outperforming proportional sampling, hand-designed schedules, and learnability-only bandits by up to 2.8 points (10% relative).

## Key Contributions

- TAC bandit: repurposes GRPO-computed per-domain advantages (learnability) and projected gradient alignment (transferability) as a bandit reward signal — no additional compute beyond the existing RL step
- Gradient-geometry transferability: measures cross-domain benefit via cosine alignment between GRPO gradient steps, identifying which domain's updates generalize broadly
- Six-domain suite: math + programming + science evaluated on Qwen3-1.7B and Llama3.2-3B; TAC wins on macro-averaged accuracy over all baselines
- Ablation confirms transferability term is load-bearing: removing it causes sharp degradation; TAC remains robust on imbalanced training mixtures

## Relevance

Directly advances the Continual RLVR thread opened by Beyond Forgetting (Nov 7) — TAC addresses the multi-domain/multi-task training curriculum problem that makes sequential RLVR inefficient, using a principled signal (gradient transferability) rather than heuristics. Also connected to the GRPO training dynamics thread (Primacy Bias, FADE) which identified that difficulty-only scheduling fails. The bandit + gradient-geometry approach generalizes to any GRPO-based multi-domain setup.

## My Thoughts

<!-- Add your own notes here -->
