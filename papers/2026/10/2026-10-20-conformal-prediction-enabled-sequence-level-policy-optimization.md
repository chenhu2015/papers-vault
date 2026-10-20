---
title: "Conformal Prediction-Enabled Sequence-level Policy Optimization for Reasoning Language Models"
authors: ["Hui Yang", "Wan Tian", "Tao Ren", "Zhongyi Li", "Yijie Peng"]
date: 2026-10-18
arxiv_id: "2610.25092"
url: "https://arxiv.org/abs/2610.25092"
score: 0.79
topics: [GRPO, RL training, PPO, reward model]
status: unread
---

# Conformal Prediction-Enabled Sequence-level Policy Optimization for Reasoning Language Models

## Summary

CSPO adaptively calibrates sequence-level clipping bounds in GRPO-style RL using conformal prediction on recent training statistics, targeting a specified marginal tail budget and adapting to policy drift rather than using fixed bands. Provides a theoretical bound on the probability of a fresh score falling outside the band via explicit CDF discrepancy and drift terms; empirically outperforms GSPO on hard math reasoning benchmarks (Qwen3-1.7B series) and ALFWorld.

## Key Contributions

- Identifies the problem of fixed clipping bands in sequence-level policy optimization: tail probabilities change as the score distribution evolves during training
- CSPO: conformal prediction calibrates clipping bounds using recent training statistics, targeting a marginal miscoverage level
- Theoretical bound on fresh-score miscoverage via CDF discrepancy and drift terms; under moment conditions, also controls objective and gradient error vs. unclipped GSPO
- Empirical improvements on MATH500, AIME, and ALFWorld with adaptive vs. fixed clipping endpoints

## Relevance

Extends the GRPO training optimization thread — a complementary direction to step-level credit assignment (SSC-GRPO, StepRS-GRPO), focusing instead on the clipping mechanism's stability problem as the policy drifts. The theoretical grounding via conformal prediction is novel in the RL-for-LLMs literature. Connects to the PRM integration cluster's theme of better-calibrated training signals.

## My Thoughts

<!-- Add your own notes here -->
