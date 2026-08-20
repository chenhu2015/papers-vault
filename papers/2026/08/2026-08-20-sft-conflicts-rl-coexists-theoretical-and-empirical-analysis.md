---
title: "SFT Conflicts, RL Coexists: A Theoretical and Empirical Analysis of Multi-Task Learning for LLMs"
authors: ["Kejian Zhu", "Zhuoran Jin", "Shangqing Tu", "Hongbang Yuan", "Yushi Bai", "Kang Liu", "Juanzi Li", "Jun Zhao"]
date: 2026-08-04
arxiv_id: "2608.03573"
url: "https://arxiv.org/abs/2608.03573"
score: 0.85
topics: [RL training, RLHF, PPO, reinforcement learning, GRPO]
status: unread
---

# SFT Conflicts, RL Coexists: A Theoretical and Empirical Analysis of Multi-Task Learning for LLMs

## Summary

Shows empirically and theoretically that SFT gradient interference is norm-limited (scales with absolute gradient magnitude), while RL gradient interference is variance-limited (bounded by the small variance from advantage normalization and on-policy optimization). This variance bound produces near-orthogonal per-task parameter updates in RL, explaining why RL enables stable multi-task coexistence while SFT causes task conflicts. Proposes Parallel-RL, which decouples multi-task RL training to improve efficiency and flexibility.

## Key Contributions

- Formal distinction: SFT interference ∝ gradient norm; RL interference ∝ gradient variance — the variance bound is what makes RL orthogonal across tasks
- Empirical confirmation at the parameter level: RL induces sparse, approximately orthogonal task-specific updates; SFT does not
- Parallel-RL paradigm: decouples multi-task RL into independent per-task training that can be composed without conflict
- Explains prior observations (why SFT catastrophically forgets, why RL training is more stable) from a single theoretical principle

## Relevance

This provides the theoretical explanation behind an empirical pattern the vault has repeatedly observed: SFT-then-RL curricula require careful ordering because SFT creates gradient conflicts that RL avoids. The Aug 17 Atomic Skills Prerequisite paper and Aug 19 SFT generalization paper both rely on empirical observations of this distinction; this paper provides the gradient-level theory. Particularly relevant to GRPO usage: GRPO's advantage normalization is the specific mechanism that bounds gradient variance and prevents task conflict.

## My Thoughts

<!-- Add your own notes here -->
