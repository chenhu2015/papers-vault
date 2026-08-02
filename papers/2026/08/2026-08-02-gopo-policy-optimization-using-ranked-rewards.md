---
title: "GOPO: Policy Optimization using Ranked Rewards"
authors: ["Kyuseong Choi", "Dwaipayan Saha", "Woojeong Kim", "Anish Agarwal", "Raaz Dwivedi"]
date: 2026-02-01
arxiv_id: "2602.03876"
url: "https://arxiv.org/abs/2602.03876"
score: 0.75
topics: [RLHF, RLAIF, GRPO, reward model, RL training]
status: unread
---

# GOPO: Policy Optimization using Ranked Rewards

## Summary

GOPO (Group Ordinal Policy Optimization) replaces GRPO's reliance on absolute reward magnitudes with a rank-based reward transformation, discarding magnitudes entirely and using only the relative ordering of rewards within a group. This addresses the misalignment between reward models (trained on relative preferences) and GRPO (which uses absolute reward values during policy optimization), yielding consistently higher reward trajectories, better LLM-as-judge evaluations, and faster convergence in non-verifiable reward settings (summarization, instruction following, chat).

## Key Contributions

- **Ordinal reward transformation**: replaces raw reward values with rank positions within the GRPO group; magnitude discarded entirely
- **Misalignment diagnosis**: reward models are trained on pairwise relative preferences but GRPO optimizes absolute magnitudes — GOPO resolves this at the signal level, not the reward model level
- **Improved convergence in non-verifiable settings**: higher training/validation reward trajectories and reaches comparable policy quality in substantially fewer steps than GRPO
- **Complementary to verifiable reward settings**: the ordinal transformation is most valuable when reward signals are non-verifiable (preference-based); for binary outcome verification, GRPO's magnitude gap is already meaningful

## Relevance

GOPO belongs to the same family as ProGPO (Aug 1 — conditional proxy substitution for all-failed groups) in that both address a structural deficiency in GRPO's reward handling, but at different failure modes: ProGPO targets all-fail groups (zero-magnitude problem), GOPO targets magnitude distortion in preference-reward settings (absolute vs. ordinal mismatch). GOPO's ordinal transformation is also relevant to the GRPO all-fail discussion: in an all-fail group, all rewards are equal, so ordinal ranking degenerates — GOPO and ProGPO are complementary fixes for complementary failure regimes.

## My Thoughts

<!-- Add your own notes here -->
