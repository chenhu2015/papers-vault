---
title: "StepOPSD: Step-Aware Online Preference Distillation for Agent Reinforcement Learning"
authors: ["Yanfei Zhang", "Xu Lin", "Chenglin Wu"]
date: 2026-06-16
arxiv_id: "2605.27140v1"
url: "http://arxiv.org/abs/2605.27140v1"
score: 0.76
topics: [reinforcement learning, GRPO, agentic RL, RL training, reward model, LLM agent]
status: unread
---

# StepOPSD: Step-Aware Online Preference Distillation for Agent Reinforcement Learning

## Summary

StepOPSD decomposes multi-turn agent trajectories into action-centered step segments, rescores them under hindsight-enriched teacher contexts, and converts token-level log-probability gaps into sign-preserving advantage shaping with a normalized per-step credit budget before the GRPO update. This step-aware preference self-distillation provides denser supervision than trajectory-level rewards without requiring external labels or gold reference trajectories, only the learner's own contrasting rollouts. Evaluated on ALFWorld and Search-QA, StepOPSD achieves first-place performance on subsets most sensitive to local causal errors including ALFWorld Heat (79.1%) and PickTwo (95.0%).

## Key Contributions

- Step-segment decomposition as the unit of credit redistribution (finer than turn-level, coarser than token-level)
- Hindsight-enriched teacher context for step rescoring — the same model at inference time with known trajectory outcome as additional context
- Sign-preserving advantage shaping with normalized per-step credit budget that integrates cleanly before GRPO update
- Empirical two-knob law: α_clip (local trust region) is broadly stabilizing; λ_mix (global mixing) is task-dependent

## Relevance

StepOPSD sits at the intersection of two threads from the past two weeks: the credit assignment cluster (Credit Assignment Survey, R3L, HiPER, AT-RL from Jun 14) and the distillation-for-RL cluster (VGS Jun 9, LiteGUI Jun 13, GAPD from today's Q3). It combines per-step granularity (like R3L's Pivotal Credit Assignment) with the self-distillation mechanism of online preference learning, creating a path to step-level dense rewards that doesn't require a trained PRM or gold trajectories.

## My Thoughts

<!-- Add your own notes here -->
