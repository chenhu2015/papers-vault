---
title: "Distributional Reward Calibration and Budget-Neutral Credit Assignment for Multimodal RLVR"
authors: ["Lang Chen", "Zongxin Xu", "Borui Wang"]
date: 2026-10-28
arxiv_id: "2610.40250v1"
url: "https://arxiv.org/abs/2610.40250"
score: 0.88
topics: [GRPO, reward model, multimodal, agentic RL, RLVR, VLM]
status: unread
---

# Distributional Reward Calibration and Budget-Neutral Credit Assignment for Multimodal RLVR

## Summary

TACE proposes a two-stage GRPO advantage estimator: at stage S1, optimal-transport distributional normalization maps each task's scalar rewards to a standard normal, eliminating cross-task reward-scale heterogeneity and capping outliers deterministically; at stage S2, rank-calibrated budget-neutral token credit redistributes the signal across tokens while conserving total credit mass and sign. The authors prove population-level inter-task moment equity, a deterministic tail bound, and mass-conservation/sign-anchoring properties that affine baselines and unnormalized token weights do not satisfy. Applied to multimodal RLVR, TACE achieves strongest results on a majority of benchmarks.

## Key Contributions

- Two-stage factorization of GRPO advantage: (S1) sample-level distributional baselining via optimal transport to standard normal; (S2) budget-neutral token credit with rank-calibration and renormalization
- Proof of population-level inter-task moment equity and deterministic tail bounds — properties affine baselines cannot satisfy
- Budget-neutrality: total credit mass and sign are conserved across the trajectory, decoupling reward scale from per-token update magnitude
- Empirical validation on multimodal reasoning suite showing best-or-near-best results across benchmarks

## Relevance

This paper bridges the VLM RL reward design thread and the step-credit cluster: it is one of the first papers to jointly address both cross-task reward calibration and intra-trajectory token credit in a principled two-stage framework specifically for multimodal RLVR. The optimal-transport normalization is a direct answer to the heavy-tail/binary-cliff reward distribution problem that affects GRPO on heterogeneous multimodal tasks.

## My Thoughts

<!-- Add your own notes here -->
