---
title: "Effective Reinforcement Learning for Agentic Search by Recycling Zero-Variance Queries During Training"
authors: ["João Coelho", "João Magalhães", "Bruno Martins", "Chenyan Xiong"]
date: 2026-06-11
arxiv_id: "2606.10709v1"
url: "http://arxiv.org/abs/2606.10709v1"
score: 0.83
topics: [agentic RL, GRPO, RL training, LLM agent]
status: unread
---

# Effective Reinforcement Learning for Agentic Search by Recycling Zero-Variance Queries During Training

## Summary

GRPO-style training discards zero-variance rollout groups (all-correct or all-incorrect) as uninformative, but this paper shows these groups dynamically flip between zero-variance and signal-bearing states as the policy evolves. Rather than discarding them, query recycling returns them to a mutable pool for policy-adaptive resampling, so the effective training distribution co-evolves with the model. A 1.7B model trained on synthetic data with recycling achieves 66.0 average Pass@1 across seven multi-hop QA benchmarks, matching or surpassing 7B models trained on benchmark-derived supervision.

## Key Contributions

- Empirical validation that zero-variance queries flip dynamically to signal-bearing as policy improves
- Mutable recycling pool: zero-variance groups returned for future policy-adaptive resampling
- 1.7B model achieves 66.0 avg Pass@1 on 7 multi-hop QA benchmarks, matching/surpassing 7B baselines
- Recycled queries supply ~75% of effective batch by training end; contributions split between policy improvement recovery and policy drift

## Relevance

Directly addresses the core training efficiency problem in GRPO-style search agent RL that the Search Agent Training Study thread flagged. This is the data-sampling complement to TRACE (same Jun 11 digest): TRACE allocates budget by turn-level contrast, query recycling ensures no prompt is permanently discarded before its time. Together they address reward contrast from two angles.

## My Thoughts

<!-- Add your own notes here -->
