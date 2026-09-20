---
title: "StepOPSD: Step-Aware Online Preference Self-Distillation for Agent Reinforcement Learning"
authors: ["Yanfei Zhang", "Xu Lin", "Chenglin Wu"]
date: 2026-05-26
arxiv_id: "2605.27140v2"
url: "http://arxiv.org/abs/2605.27140v2"
score: 0.87
topics: [agentic RL, GRPO, RL training, reward model, LLM agent]
status: unread
---

# StepOPSD: Step-Aware Online Preference Self-Distillation for Agent Reinforcement Learning

## Summary

StepOPSD treats the agent step as the unit of credit redistribution in multi-turn RL, decomposing trajectories into action-centered step segments and rescoring them under hindsight-enriched teacher contexts. Token-level log-probability gaps are converted into sign-preserving advantage shaping with a normalized per-step credit budget before the GRPO update. Results on ALFWorld and Search-QA reveal a two-knob law: smaller α_clip acts as a broadly stabilizing trust region, while optimal λ_mix remains task-dependent.

## Key Contributions

- Action-centered step segmentation: trajectories split at agent action boundaries rather than token or turn boundaries
- Hindsight-enriched teacher rescoring at the step level, providing denser credit than trajectory-level OPD
- Sign-preserving advantage shaping with a normalized per-step credit budget — preserves verifier-determined direction while redistributing magnitude
- Empirical two-knob law: α_clip stabilizes broadly (task-agnostic), λ_mix requires task-specific tuning

## Relevance

Directly follows up the AHEAD thread (Sep 19): where AHEAD classifies steps by type (routine vs critical error), StepOPSD uses action-centered segmentation as the credit unit with hindsight rescoring. The two form a complementary pair — AHEAD's step-type classification axis vs StepOPSD's action-boundary axis — within the broader hindsight distillation cluster (TRIAL/T-STAR/TASPO/CRISP/VICT/HiMPO/AHEAD, now 8 entries). Found via step-type hindsight follow-up query targeting AHEAD adjacency.

## My Thoughts

<!-- Add your own notes here -->
