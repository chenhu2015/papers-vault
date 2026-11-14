---
title: "Scaf-GRPO: Scaffolded Group Relative Policy Optimization for Enhancing LLM Reasoning"
authors: ["Xichen Zhang", "Sitong Wu", "Yinghao Zhu", "Haoru Tan", "Shaozuo Yu", "Ziyi He", "Jiaya Jia"]
date: 2025-10-22
arxiv_id: "2510.19807v2"
url: "https://arxiv.org/abs/2510.19807"
score: 0.78
topics: [agentic RL, RL training, GRPO, RLVR, reinforcement learning]
status: unread
---

# Scaf-GRPO: Scaffolded Group Relative Policy Optimization for Enhancing LLM Reasoning

## Summary

Scaf-GRPO addresses the learning cliff where models consistently fail on hard problems, collapsing GRPO advantage to zero. It monitors for learning stagnation and intervenes by injecting tiered in-prompt hints (from abstract concepts to concrete steps) only when independent learning has plateaued — strategic minimal guidance rather than constant scaffolding. On Qwen2.5-Math-7B, Scaf-GRPO achieves a 44.3% relative improvement on AIME24 over vanilla GRPO. This is distinct from AutoScaffold (frozen teacher continuously generates scaffolds) in its detect-stagnation-then-inject trigger mechanism.

## Key Contributions

- Diagnoses the learning cliff: when all rollouts fail on hard problems, GRPO advantage collapses to zero, stalling progress
- Stagnation detection: monitors when model's independent exploration has plateaued without improvement
- Tiered hint injection: provides minimal intervention (abstract concepts → concrete steps) only after stagnation is confirmed, preserving autonomous exploration otherwise
- +44.3% relative improvement on AIME24 (Qwen2.5-Math-7B) over vanilla GRPO baseline

## Relevance

Seventh entry in the adaptive scaffolding cluster (AutoScaffold, JoMoHa, Targeted Guidance, SkillScaffold, Agent-G², METIS, Scaf-GRPO). Scaf-GRPO's specific contribution is the stagnation-triggered injection mechanism — different from METIS (metacognitive curriculum) and Targeted Guidance (failure-gated distillation): here the intervention fires when the model is stuck on the learning curve, not when individual rollouts fail. The connection to PICO (also found this day) is notable: both address the zero-advantage problem on hard problems but via different mechanisms (token-level policy-compatible decoding vs. in-prompt hint injection).

## My Thoughts

<!-- Add your own notes here -->
