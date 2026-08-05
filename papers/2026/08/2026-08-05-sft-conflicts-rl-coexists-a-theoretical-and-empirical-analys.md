---
title: "SFT Conflicts, RL Coexists: A Theoretical and Empirical Analysis of Multi-Task Learning for LLMs"
authors: ["Kejian Zhu", "Zhuoran Jin", "Shangqing Tu", "Hongbang Yuan", "Yushi Bai", "Kang Liu", "Juanzi Li", "Jun Zhao"]
date: 2026-08-05
arxiv_id: "2608.03573"
url: "https://arxiv.org/abs/2608.03573"
score: 0.86
topics: [reinforcement learning, RL training, agentic RL, RLHF, RLAIF, GRPO]
status: unread
---

# SFT Conflicts, RL Coexists: A Theoretical and Empirical Analysis of Multi-Task Learning for LLMs

## Summary

This paper reveals that SFT suffers from severe task conflicts under multi-stage multi-task LLM training while RL enables stable coexistence, tracing the difference to parameter-level dynamics: RL induces sparse, approximately orthogonal gradient updates across tasks. Theoretically, interference in SFT is norm-limited (scales with gradient magnitude), whereas interference in RL is variance-limited (bounded by the gradient variance from advantage normalization and on-policy optimization), yielding near-orthogonal optimization directions. Building on this insight, the authors propose Parallel-RL, a paradigm that decouples multi-task RL training for improved efficiency and flexibility.

## Key Contributions

- Empirical observation: SFT shows severe task conflicts under multi-stage multi-task training while RL stably coexists across diverse tasks
- Theoretical proof: interference in SFT is norm-limited (scales with absolute gradient magnitude) vs. interference in RL is variance-limited (bounded by advantage normalization + on-policy optimization variance)
- Parallel-RL: a multi-task RL paradigm that exploits near-orthogonal RL gradients to decouple task training for efficiency and flexibility

## Relevance

This paper directly addresses Gap #1 (adaptive SFT→RL interleaving) by providing a theoretical explanation for *why* RL is structurally superior to SFT for multi-task settings: advantage normalization in GRPO/PPO induces bounded gradient variance, which in turn makes cross-task gradient interference near-orthogonal. This is the first paper in the vault to provide a formal mechanism for this SFT vs. RL distinction in multi-task reasoning, which has been searched for since July 28 without success.

## My Thoughts

<!-- Add your own notes here -->
