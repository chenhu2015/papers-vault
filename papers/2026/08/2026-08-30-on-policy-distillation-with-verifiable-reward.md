---
title: "On-policy Distillation with Verifiable Reward"
authors: ["Wenze Lin", "Jiale Zhao", "Xitai Jiang", "Songde Rao", "Yining Li", "Shenzhi Wang", "Bingxiang He", "Gao Huang"]
date: 2026-08-30
arxiv_id: "2608.24696"
url: "https://arxiv.org/abs/2608.24696"
score: 0.81
topics: [RLHF, RLAIF, PPO, GRPO, agentic RL, RL training, LLM agent]
status: unread
---

# On-policy Distillation with Verifiable Reward

## Summary

Proposes OPDVR, which fuses on-policy distillation (OPD) and Reinforcement Learning with Verifiable Rewards (RLVR) without extra hyperparameters by reformulating OPD's implicit reward as trajectory-correctness-conditioned: a ReLU gating mechanism ensures correct trajectories receive non-negative distillation rewards and incorrect ones receive non-positive rewards, aligning dense token-level supervision with verifiable task success. This transforms sampled-token OPD into a proper RLVR method, making it directly composable with GRPO; six reasoning benchmark evaluations show consistent improvement over standard OPD.

## Key Contributions

- Trajectory-correctness-gated reformulation of OPD implicit reward — no new hyperparameters
- ReLU gating: correct trajectory → non-negative reward, incorrect → non-positive reward, preserving teacher distributional guidance while adding task-level correctness signal
- Makes sampled-token OPD a proper RLVR method, composable with any policy gradient algorithm including GRPO
- Addresses the same OPD/RLVR integration problem as AToD (Aug 29) but algebraically rather than through a temporal annealing schedule

## Relevance

The OPD/RLVR hybrid thread in the vault now has two approaches: AToD (annealed schedule, transitions from OPD to RL over training) and OPDVR (algebraic gating, both signals active throughout). OPDVR's approach is hyperparameter-free and aligns directly with the GRPO training loop seen in SRPO, IAPO, and SPO++. The comparison of these two integration strategies on shared benchmarks is an open empirical gap — both claim to solve the same problem with different inductive biases (temporal schedule vs. per-trajectory gating).

## My Thoughts

<!-- Add your own notes here -->
