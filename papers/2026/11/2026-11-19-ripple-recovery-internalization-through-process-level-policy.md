---
title: "RIPPLE: Recovery Internalization through Process-Level Policy Learning and Effect-Aware Credit for Long-Horizon Agentic Coding"
authors: ["Jingxuan Xu", "Zihang Xu", "Yuechen Luo", "Ziqi Miao", "Wenqiang Zhu"]
date: 2026-10-22
arxiv_id: "2610.31276"
url: "https://arxiv.org/abs/2610.31276"
score: 0.86
topics: [agentic RL, RL training, LLM agent, agentic, reward model]
status: unread
---

# RIPPLE: Recovery Internalization through Process-Level Policy Learning and Effect-Aware Credit for Long-Horizon Agentic Coding

## Summary

RIPPLE addresses the Critique-to-Action Handoff Gap in long-horizon coding agents, where agents observe failures and generate plausible critiques but continue down the same incorrect trajectory. It uses a prefix-only teacher for evidence-grounded recovery supervision, then applies RL with stage-specific credit assignment across reflection triggering, diagnosis, and corrective action. Local validity signals gate trajectory advantages so intermediate recovery steps do not indiscriminately inherit terminal outcomes, improving recovery rates across four repository-level benchmarks by 4.8 score points on average.

## Key Contributions

- Critique-to-Action Handoff Gap: identifies and names the failure mode where critique generation and corrective action remain decoupled in long-horizon agents
- Process-level policy learning with prefix-only teacher: provides evidence-grounded recovery supervision without access to future actions or terminal outcomes
- Stage-specific effect-aware credit: separate credit for reflection triggering, diagnosis, and corrective action — avoids conflating distinct recovery sub-tasks
- Local validity gating: intermediate recovery advantages are gated by local validity signals, not inherited indiscriminately from terminal outcomes

## Relevance

RIPPLE is adjacent to EMPO (which identified credit-update misalignment across executably equivalent responses) and to the multi-turn OPSD cluster. It introduces a new failure mode taxonomy specific to recovery in coding agents, and its effect-aware credit mechanism connects to EMPO's effect-level surrogate and to RIPPLE's stage-decomposed process supervision — the EMPO adjacent search thread from Nov 18's Tomorrow plan.

## My Thoughts

<!-- Add your own notes here -->
