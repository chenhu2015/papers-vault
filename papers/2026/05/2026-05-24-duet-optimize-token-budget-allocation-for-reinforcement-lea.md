---
title: "DUET: Optimize Token-Budget Allocation for Reinforcement Learning with Verifiable Rewards"
authors: ["Haoyu Hu", "Xuandong Zhao", "Xuhai \"Orson\" Xu", "Nori Jacoby"]
date: 2026-05-08
arxiv_id: "2605.08441v1"
url: "http://arxiv.org/abs/2605.08441v1"
score: 0.86
topics: [GRPO, RL training, agentic RL, reward model, reinforcement learning]
status: unread
---

# DUET: Optimize Token-Budget Allocation for Reinforcement Learning with Verifiable Rewards

## Summary

DUET jointly optimizes two orthogonal token-budget axes in RLVR: which prompts receive rollouts (via a lightweight pre-rollout surrogate of prompt informativeness) and when to stop each rollout (via a marker-gated abort rule with importance reweighting). Prior methods control only one dimension at a time. Using just 50% of the token budget, DUET still outperforms all full-budget baselines—including GRPO and three budget-aware methods—on math, coding, and science QA, delivering a 2.51× wall-clock speedup.

## Key Contributions

- Dual-controlled token allocation framework: joint prompt selection + per-rollout length control under a shared compute budget
- Lightweight pre-rollout surrogate estimates prompt informativeness to allocate rollout counts per prompt
- Marker-gated abort rule with importance reweighting determines when to stop individual rollouts
- Empirically validated on Qwen3-1.7B, Qwen3-4B, and Llama-3.2-3B-Instruct; efficiency gap widens as budget tightens

## Relevance

Directly addresses the long-sought "reasoning budget RL" thread that failed as a search target for 3+ consecutive days (May 21–23); DUET's dual-axis control is the orthogonal budget-management complement to GRPO algorithm variants and length-penalty methods already covered.

## My Thoughts

<!-- Add your own notes here -->
