---
title: "Reconciling Process Supervision with Outcome-Based Credit in Agentic Policy Optimization"
authors: ["Jingxiao Yang", "Wangjie Gan", "Yingxuan Zhuang", "Wenqi Zhang", "Jintao Chen", "Xuhong Zhang"]
date: 2026-08-31
arxiv_id: "2608.31077v1"
url: "https://arxiv.org/abs/2608.31077"
score: 0.83
topics: [agentic RL, RL training, RLHF, reward model, GRPO]
status: unread
---

# Reconciling Process Supervision with Outcome-Based Credit in Agentic Policy Optimization

## Summary

TASPO identifies the supervision-credit gap in process-supervised agentic RL: PI-induced likelihood changes describe information value but do not determine how an action should inherit verified outcome credit. It constructs decision-applicable privileged information (PI) from verified successful experience, aggregates PI-induced likelihood shifts at the executable-action level, and converts relative action support into mean-preserving weights on the original trajectory advantage — verified outcome determines update direction and scale while PI only redistributes credit across actions. TASPO improves over GRPO by 10.6% on three agentic benchmarks.

## Key Contributions

- Supervision-credit gap: formal identification that fine-grained process supervision (PI-induced likelihood changes) is not equivalent to fine-grained credit — PI signals may be irrelevant to current state, operate at wrong granularity, or lack outcome semantics
- Decision-applicable PI construction: PI is filtered and aggregated at the executable-action level from verified successful experience, not raw process annotations
- Mean-preserving weight redistribution: PI-induced relative action support → bounded, mean-preserving weights on original trajectory advantage — outcome determines average update magnitude, PI only redistributes within-trajectory
- +10.6% over GRPO across three agentic benchmarks with better generalization to unseen tasks

## Relevance

TASPO is the formal bridge between the process supervision thread (ExecCritic, ERPO from Sep 09) and the credit assignment thread (TRIAL, RTPO, T-STAR from Sep 07-08). It resolves the conceptual gap that ExecCritic and ERPO left open: both use execution outcomes as reward, but neither addresses how process-level signals should be weighted against verified terminal outcomes. TASPO's mean-preserving constraint is structurally similar to GRPO's group normalization — it preserves the outcome-determined gradient scale while fine-graining within it.

## My Thoughts

<!-- Add your own notes here -->
