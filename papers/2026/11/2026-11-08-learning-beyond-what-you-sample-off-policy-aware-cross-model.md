---
title: "Learning Beyond What You Sample: Off-Policy-Aware Cross-Model Trajectory Exchange for RLVR"
authors: ["Doohyuk Jang", "Yoonsik Park", "Gyouk Chu", "Sihwan Park", "Eunho Yang"]
date: 2026-09-29
arxiv_id: "2609.37868v1"
url: "https://arxiv.org/abs/2609.37868"
score: 0.82
topics: [GRPO, RLHF, RL training, agentic RL, reward model]
status: unread
---

# Learning Beyond What You Sample: Off-Policy-Aware Cross-Model Trajectory Exchange for RLVR

## Summary

GRAFT addresses the all-fail group problem in GRPO — where finite rollout budgets produce groups with no reward-gradient signal — by replacing empty groups with peer trajectories from heterogeneous models that succeed on complementary prompts. Cross-model mismatch is controlled via sequence-level compatibility weighting and token-level importance ratio clipping, allowing both successful and unsuccessful peer responses with peer-computed advantages to transfer safely. Across three heterogeneous model pairs and five math benchmarks, GRAFT consistently improves both models over GRPO with the same per-model rollout budget, gaining 2.1pp on average and up to 4.5pp.

## Key Contributions

- Exploits complementary success patterns: different models systematically succeed on different problem subsets, making peer trajectory exchange more reliable than additional self-rollouts
- Sequence-level compatibility weighting + token-level importance ratio clipping: dual off-policy correction that controls cross-model mismatch without full importance sampling overhead
- Mutual benefit: GRAFT improves both participating models simultaneously, unlike teacher-student setups
- Stored peer trajectory mode: preserves most gains (+1.8pp over GRPO) without simultaneous co-training, enabling asynchronous use

## Relevance

Directly connects to the GRPO training dynamics thread's all-fail group problem (also addressed by CREDO's evidence-conditioned credit from Nov 7). GRAFT takes a complementary approach — instead of recovering supervision within all-fail groups, it eliminates them by importing successful trajectories from peers. The off-policy correction connects to the DLC/VeXact TIM thread: importance ratio clipping is the same mechanism DLC uses to manage policy lag. TAC (also Nov 8) addresses a related challenge from the curriculum angle.

## My Thoughts

<!-- Add your own notes here -->
