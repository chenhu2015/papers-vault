---
title: "ATOD: Annealed Turn-Aware On-Policy Distillation for Multi-Turn Agentic Tasks"
authors: ["Qitai Tan", "Zefang Zong", "Mo Li", "Yipeng Shi", "Yang Li", "Peng Chen"]
date: 2026-06-26
arxiv_id: "2606.27814"
url: "https://arxiv.org/abs/2606.27814"
score: 0.82
topics: [agentic RL, RL training, LLM agent, GRPO]
status: unread
---

# ATOD: Annealed Turn-Aware On-Policy Distillation for Multi-Turn Agentic Tasks

## Summary

ATOD proposes an annealed training schedule where on-policy distillation from a teacher dominates early training for fast convergence, then RL is gradually strengthened to push past the teacher's ceiling — two phases that compete on all prior hybrid approaches but here complement each other cleanly. A Turn-level Disagreement-Uncertainty Reweighting (T-DUR) module gates the distillation signal to prioritize turns where student and teacher diverge most, improving credit efficiency in long trajectories. On ALFWorld, WebShop, and Search-QA, ATOD improves 4.16 points over pure OPD and 23.62 points over GRPO in average success rate, and surpasses the teacher model itself by 2.16 points.

## Key Contributions

- Annealed OPD→RL schedule: OPD dominates early training (fast convergence to teacher-level), RL weight increases monotonically (drives reward-based exploration beyond teacher ceiling)
- T-DUR: Turn-level Disagreement-Uncertainty Reweighting that softly gates distillation signal by per-turn disagreement and uncertainty, focusing supervision on the most informative trajectory segments
- Beats teacher model by 2.16 points — the annealing enables the student to exceed the teacher, not just match it
- Evaluated on ALFWorld, WebShop, Search-QA across three student model sizes

## Relevance

Directly advances the agentic RL + RL training core interests and connects to the large on-policy self-distillation cluster in the vault (BCSD, NOPD, OGLS-SD, GC-OPD, etc.). While those papers focus on distillation architecture, ATOD focuses on the training dynamics — when to distill vs. when to reinforce — which is the temporal scheduling problem none of the prior vault OPD papers address as their primary contribution.

## My Thoughts

<!-- Add your own notes here -->
