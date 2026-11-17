---
title: "Rethinking On-Policy Self-Distillation for Thinking Models"
authors: ["(see arxiv 2607.05184)"]
date: 2026-07-06
arxiv_id: "2607.05184"
url: "https://arxiv.org/abs/2607.05184"
score: 0.88
topics: [RL training, RLHF, OPSD, thinking models]
status: unread
---

# Rethinking On-Policy Self-Distillation for Thinking Models

## Summary

Shows that OPSD specifically degrades thinking models (Qwen3, OLMo) on long reasoning traces, with up to 17% relative accuracy drop on AIME24/25/HMMT25. Mechanistically, privileged teacher context suppresses exploration at high-entropy forking positions — the positions where thinking models derive their largest gains. Distillation from a larger privileged teacher reverses OPD's gains on thinking models, while helping instruction-tuned models, suggesting a fundamental incompatibility between OPSD and the internal deliberation mechanisms of thinking models.

## Key Contributions

- Demonstrates that OPSD degrades thinking models at scale across five model families and three hard benchmarks
- Identifies high-entropy forking positions as the mechanistic site: privileged context lowers fork rates in thinking models but not instruction-tuned models
- Shows that at self-correction branches, privileged OPD penalizes reconsideration tokens that vanilla OPD supports
- Thinking models trained with privileged teacher produce fewer verification, backtracking, and hedging markers even after length normalization

## Relevance

Extends the OPSD diagnostic cluster (Diagnosing OPSD + OASIS + HATCH from Nov 16) with a new failure dimension: thinking models are specifically harmed. Where Diagnosing OPSD (Nov 16) showed four generic failure modes, this paper identifies a qualitatively distinct mechanism for thinking models — the suppression of deliberative exploration that is unique to thinking-model rollouts. Together, these papers suggest that OPSD's core PI assumption is fundamentally incompatible with strong thinking models.

## My Thoughts

<!-- Add your own notes here -->
