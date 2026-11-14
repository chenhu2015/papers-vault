---
title: "Outcome-Mass Alignment: Controlling Length-Dependent Trajectory Influence in Multi-Turn LLM Agent Reinforcement Learning"
authors: ["Dawei Zhang", "Yubin Huangfu", "Jessica Fan", "Boyu Wei", "Likang Wu", "Hongke Zhao", "Ming He", "Zhu Teng"]
date: 2026-11-12
arxiv_id: "2611.16816v1"
url: "https://arxiv.org/abs/2611.16816"
score: 0.80
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# Outcome-Mass Alignment: Controlling Length-Dependent Trajectory Influence in Multi-Turn LLM Agent Reinforcement Learning

## Summary

OMA (Outcome-Mass Alignment) identifies two implicit weighting pathologies in multi-turn GRPO: outcome-statistics multiplicity (one episode outcome counted multiple times across expanded trajectory rows) and objective-mass imbalance (failed trajectories expand much more than successful ones, assigning them disproportionate gradient mass). Its two-component fix separates outcome statistics over unique source trajectories from aggregate mass control after within-trajectory reduction. On ALFWorld with GRPO, OMA improves matched-horizon endpoint success by 7.0–9.4 percentage points across two model scales.

## Key Contributions

- Identifies outcome-statistics multiplicity: multi-turn GRPO materializes each trajectory into multiple rows, causing one outcome to be counted multiple times in group statistics
- Identifies objective-mass imbalance: failed trajectories (more tokens/steps) expand more than successful ones, inadvertently receiving more gradient mass
- Outcome Alignment: computes outcome statistics over unique source trajectories rather than expanded rows
- Mass Alignment: controls aggregate objective mass after within-trajectory reduction, independent of trajectory expansion ratio

## Relevance

Directly relevant to the GRPO training dynamics thread and agentic RL — this is a unique paper in that it identifies problems introduced *specifically* by multi-turn trajectory materialization in GRPO, which is distinct from single-turn GRPO mechanics. Complements the broader GRPO accounting corrections thread (LGPO, BRAT) and extends the multi-turn agentic RL literature (ALFWorld experiments connect to AutoScaffold, JoMoHa, SkillScaffold, Agent-G² cluster).

## My Thoughts

<!-- Add your own notes here -->
