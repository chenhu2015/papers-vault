---
title: "ARMOR: Stabilizing On-Policy LLM RL with Off-Policy Anchor Samples"
authors: ["Kexin Huang", "Junkang Wu", "Jinda Lu"]
date: 2026-07-28
arxiv_id: "2607.10481"
url: "https://arxiv.org/abs/2607.10481"
score: 0.75
topics: [RL training, GRPO, PPO, reward model, LLM agent]
status: unread
---

# ARMOR: Stabilizing On-Policy LLM RL with Off-Policy Anchor Samples

## Summary

Identifies over-optimization (models exploiting training heuristics at the expense of generalizable reasoning) as a critical instability source in LLM RL, and shows that standard reverse-KL regularization is insufficient because it fails to ensure reference-distribution coverage. ARMOR (Anchor Rollout and Mixed Optimization for RL) addresses this with off-policy data from the reference policy (Anchor Rollout) to preserve established solution patterns, combined with a reformulated policy objective (Mixed Optimization) for controlled exploration without auxiliary losses.

## Key Contributions

- Diagnostic: reverse-KL regularization insufficient for coverage — can satisfy reverse-KL constraint while still drifting from reference distribution's solution patterns
- Anchor Rollout: off-policy data sampled from the reference policy mixed into the training batch to preserve established high-quality solution diversity
- Mixed Optimization: reformulated policy objective enabling controlled exploration that doesn't rely on auxiliary losses
- Validated on reasoning benchmarks showing sustained performance improvement over extended training horizons without validation collapse

## Relevance

Addresses the over-optimization / validation collapse instability that is mechanistically distinct from GRPO's all-fail group amplification (Dark Room, Jul 25) and clipping pathologies (Clip-Low/Clip-High, Jul 24) — ARMOR's off-policy anchor approach provides a sample-diversity stabilization mechanism, complementary to variance-profile-based reward signal design (Dark Room) and orthogonal to the credit assignment thread; most closely related to SEED (Jul 26) which uses hindsight trajectories as auxiliary signals, but ARMOR uses reference-policy samples rather than completed trajectories.

## My Thoughts

<!-- Add your own notes here -->
