---
title: "FSPO: Policy-Consistent Risk and Pareto-Feasible Control for Budgeted LLM RL Post-Training"
authors: ["Miaobo Hu", "Shuhao Hu", "Xiaobo Guo", "Xin Wang", "Bokun Wang", "Daren Zha"]
date: 2026-10-02
arxiv_id: "2610.02828v2"
url: "http://arxiv.org/abs/2610.02828v2"
score: 0.81
topics: [GRPO, PPO, RL training, reinforcement learning, reward model]
status: unread
---

# FSPO: Policy-Consistent Risk and Pareto-Feasible Control for Budgeted LLM RL Post-Training

## Summary

FSPO is a feedback-state controller that jointly adapts multiple RL training actuators online (rollout temperature, group size, clipping, KL regularization, verifier allocation, update budget) while addressing three coupled issues: policy-distribution mismatch in risk models, calibration drift under selective actions, and infeasible multi-resource continuations. It introduces a policy-consistent risk-to-go model (PRCC), decision-conditioned trajectory calibration (DCTC), and a Pareto resource continuation certificate, achieving +2.42/+3.19 pp over the strongest contextual-bandit baseline on held-out and OOD evaluation.

## Key Contributions

- Policy-consistent risk-to-go model: Bellman target follows the same frozen controller used for future decisions, avoiding deployment mismatch
- DCTC (Decision-Conditioned Trajectory Calibration): calibrates risk on cross-fitted trajectories from provisional controllers; lowers ECE from 0.039 to 0.022
- PRCC (Pareto Resource Continuation Certificate): admits actions only when non-dominated cumulative reservation remains feasible; eliminates false-feasible admissions (0.197→0.000)
- Joint control of 6+ RL training actuators, achieving 66.11%/59.43% held-out/OOD vs 64.47%/57.03% for PB2

## Relevance

Directly follows the LLMZero adaptive training dynamics thread: where LLMZero discovers adaptive GRPO strategies via tree search, FSPO provides a rigorous feedback-state control framework with formal feasibility guarantees — complementary approaches to the same problem of adaptive multi-actuator RL training.

## My Thoughts

<!-- Add your own notes here -->
