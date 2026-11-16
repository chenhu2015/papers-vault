---
title: "SAGE-OPD: Selective Agent-Guided Intervention for Multi-Turn On-Policy Distillation"
authors: ["Yuhang Zhou", "Lizhu Zhang", "Yifan Wu", "Mingyi Wang", "Bo Peng", "Jiayi Liu", "Xiangjun Fan", "Zhuokai Zhao"]
date: 2026-06-17
arxiv_id: "2606.19659v1"
url: "https://arxiv.org/abs/2606.19659"
score: 0.84
topics: [agentic RL, LLM agent, GRPO, RL training, agentic]
status: unread
---

# SAGE-OPD: Selective Agent-Guided Intervention for Multi-Turn On-Policy Distillation

## Summary

SAGE-OPD addresses multi-turn OPD's compounding-error problem by selectively applying teacher intervention only at turns where feedback indicates it's necessary, weighted by teacher confidence to reduce influence of uncertain distributions on corrupted histories. Loss normalization preserves overall loss scale while enabling turn-level selectivity, complementing rather than replacing the standard OPD objective. Achieves +13.3% relative improvement in ALFWorld unseen success rate over standard OPD, with ablations confirming each design decision contributes independently.

## Key Contributions

- Turn-level selective intervention: applies teacher OPD supervision only where environment feedback signals failure, not uniformly across all turns
- Teacher confidence weighting: down-weights teacher supervision on turns with corrupted or ambiguous observation histories
- Loss normalization: preserves OPD's loss scale under selective supervision to prevent training instability
- Ablation confirming 3-way independence: selection, confidence weighting, and normalization each contribute separately

## Relevance

Extends the "when to trust the teacher" cluster (GIFT + ECOS + SAGE-OPD) to the multi-turn agentic setting with a verifier-free mechanism. ECOS uses environment-calibrated outcome-based weighting; GIFT uses gradient geometry; SAGE-OPD uses turn-level teacher-confidence weighting on the multi-turn trajectory. The three mechanisms are orthogonal and potentially composable. SAGE-OPD also bridges the adaptive scaffolding cluster (selective injection at needed turns) and the RL+distillation compatibility cluster (how to avoid propagating unreliable teacher supervision).

## My Thoughts

<!-- Add your own notes here -->
