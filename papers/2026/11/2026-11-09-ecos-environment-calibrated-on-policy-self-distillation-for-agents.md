---
title: "ECOS: Environment-Calibrated On-Policy Self-Distillation for Language Agents"
authors: ["Chenhao Zhang", "Zhongan Wang", "Mingxuan Li"]
date: 2026-11-09
arxiv_id: "2611.12232"
url: "https://arxiv.org/abs/2611.12232"
score: 0.84
topics: [agentic RL, LLM agent, tool use, GRPO, RLHF]
status: unread
---

# ECOS: Environment-Calibrated On-Policy Self-Distillation for Language Agents

## Summary

ECOS fixes a fundamental failure mode in on-policy self-distillation for language agents: existing methods weight teacher guidance by token likelihood shift rather than behavioral improvement, so errors in self-written skills compound over training because the teacher confidently endorses its own mistakes. ECOS uses environmental outcomes to estimate command-level advantages (comparing outcomes at similar observations) and reweights teacher preferences toward high-advantage trajectories, additionally filtering supervision to executable commands only. Results: 93.3% ALFWorld and 80.5% WebShop on 7B, outperforming GRPO by +7.6pp on unseen ALFWorld tasks.

## Key Contributions

- Diagnosis: existing OPSD weights guidance by likelihood shift, not behavior improvement → error compounding
- Command-level advantages estimated by comparing outcomes at similar observations (environment-calibrated)
- Teacher preferences scaled by advantage; reflections and skills whose preferences favor higher-advantage commands are reinforced
- Supervision filtered to executable commands only (removes full-response noise); 52.3% → 75.0% WebShop on 3B
- 90.5%/93.3% ALFWorld seen, 75.5%/80.5% WebShop on 3B/7B; +11.0/7.6pp over GRPO on unseen ALFWorld

## Relevance

Directly extends the adaptive scaffolding cluster (AutoScaffold, JoMoHa, Targeted Guidance, SkillScaffold, Agent-G², METIS, Scaf-GRPO) with a new mechanism: behavioral-outcome-based filtering of self-generated teacher guidance. The environment-calibrated advantage approach is distinct from all prior cluster entries and addresses the error-compounding failure mode that makes naive OPSD worse than pure GRPO in some regimes.

## My Thoughts

<!-- Add your own notes here -->
