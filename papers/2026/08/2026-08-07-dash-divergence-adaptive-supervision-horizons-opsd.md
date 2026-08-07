---
title: "DASH: Divergence-Adaptive Supervision Horizons for On-Policy Self-Distillation of Reasoning Models"
authors: ["ZhiYan Hou", "Xinyu Tang", "Hongyan An", "Jianjin Zhang"]
date: 2026-08-06
arxiv_id: "2608.06243v1"
url: "https://arxiv.org/abs/2608.06243"
score: 0.86
topics: [agentic RL, RLHF, reward model, LLM agent]
status: unread
---

# DASH: Divergence-Adaptive Supervision Horizons for On-Policy Self-Distillation of Reasoning Models

## Summary

DASH addresses a key limitation of standard OPSD: assigning uniform supervision weight regardless of how local divergences evolve across the rollout trajectory. It maps each token's local divergence deviation from the sequence mean to an adaptive propagation gate, then uses these gates for backward multi-step aggregation — effectively weighting token-level supervision by temporal divergence context rather than local magnitude alone. This introduces a 4th orthogonal calibration axis for OPSD beyond OCSD (scaffold isolation), PCSD (temporal persistence), and ADRS (confidence-return correlation): the sequential divergence history surrounding each token.

## Key Contributions

- Identifies that standard OPSD treats all local divergences uniformly regardless of their temporal context (position within the discrepancy sequence)
- Adaptive propagation gate: maps each token's local divergence deviation from the sequence mean to a weight, then applies backward multi-step aggregation
- No additional teacher or student forward passes required — reuses existing OPSD distributions
- Improvements over matched vanilla OPSD reruns on all 3 math benchmarks at all 3 model scales

## Relevance

DASH introduces the 4th orthogonal axis for OPSD teacher calibration, complementing OCSD (scaffold isolation, Aug 6), PCSD (temporal persistence), and ADRS (confidence-return correlation, Aug 5). The vault's Gap #19 focused on a 3-way A×B×C calibration gate combining ADRS-TVA × PCSD-persistence × OCSD-scaffold; DASH adds a 4th axis D: sequential divergence history context. A combined A×B×C×D gate would be the most complete teacher calibration framework described in the vault to date.

## My Thoughts

<!-- Add your own notes here -->
