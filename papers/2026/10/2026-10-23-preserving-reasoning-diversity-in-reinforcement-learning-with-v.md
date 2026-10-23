---
title: "Preserving Reasoning Diversity in Reinforcement Learning with Verifiable Rewards via Adaptive Replay"
authors: ["Wen-Zhi Li", "Sainyam Galhotra", "Claire Cardie"]
date: 2026-10-16
arxiv_id: "2610.24236v1"
url: "https://arxiv.org/abs/2610.24236"
score: 0.76
topics: [RLHF, RLAIF, RL training, GRPO]
status: unread
---

# Preserving Reasoning Diversity in Reinforcement Learning with Verifiable Rewards via Adaptive Replay

## Summary

TAR (Targeted Adaptive Replay) addresses mode collapse in RLVR by maintaining a compact memory bank of diverse base-model solutions and selectively replaying suppressed reasoning modes during on-policy training. Shows that finite-sample rollout dynamics progressively starve semantically distinct but equally-rewarded strategies; TAR recovers this diversity with minimal overhead across 6 math benchmarks and 2 Qwen2.5 scales.

## Key Contributions

- Theoretical analysis showing finite-sample on-policy RLVR progressively suppresses under-sampled but correct reasoning modes once below a recovery threshold
- TAR: compact memory bank of diverse base-model solutions + adaptive replay trigger that activates only when stored modes are being suppressed
- Consistent improvement on both reasoning performance and diversity preservation vs. existing methods across Qwen2.5-7B and Qwen2.5-14B
- Substantially reduces forgetting of correct base-model solutions compared to vanilla RLVR

## Relevance

Complements the Preserving Reasoning Diversity angle that TAR addresses the other side of the RLVR mode-collapse coin from CSPO (Oct 20, GRPO clipping calibration) — CSPO prevents gradient instability while TAR prevents strategy starvation. Both are training-stability contributions to the GRPO/RLVR cluster.

## My Thoughts

<!-- Add your own notes here -->
