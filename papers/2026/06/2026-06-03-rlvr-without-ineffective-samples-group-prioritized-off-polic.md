---
title: "RLVR without Ineffective Samples: Group Prioritized Off-Policy Optimization for LLM Reasoning"
authors: ["Yixiu Mao", "Yun Qu", "Qi Wang", "Heming Zou", "Xiangyang Ji"]
date: 2026-06-03
arxiv_id: "2606.01281"
url: "https://arxiv.org/abs/2606.01281"
score: 0.87
topics: [GRPO, RLVR, reinforcement learning, reward model, LLM agent, PPO]
status: unread
---

# RLVR without Ineffective Samples: Group Prioritized Off-Policy Optimization for LLM Reasoning

## Summary

POPO addresses the fundamental inefficiency of RLVR training where zero-variance reward groups (all-correct or all-incorrect rollout batches) provide no learning signal, by replacing them with effective off-policy rollouts via a recency-based prioritized replay mechanism. It pairs this with decoupled importance sampling that corrects off-policy bias while enforcing consistent trust-region constraints. Evaluated on math, planning, and visual geometry, POPO achieves strong reasoning performance with significantly fewer on-policy rollouts than GRPO/PPO baselines.

## Key Contributions

- Identifies and quantifies the "ineffective sample" problem in RLVR: a large fraction of training batches yield zero-variance rewards, wasting rollout compute
- Prioritized group replay: replaces zero-variance on-policy groups with effective off-policy groups using a recency-aware buffer that jointly considers sample quality and off-policiness degree
- Decoupled importance sampling: corrects off-policy distributional shift while maintaining stable trust-region constraints (not blending IS into the same loss term)
- Demonstrates substantial rollout reduction without accuracy loss across math, planning, and visual geometry benchmarks

## Relevance

Directly follows the carry-forward from the June 2 digest (ReVal off-policy LLM RL thread) and targets the exact training inefficiency that makes on-policy GRPO expensive. Complements EP-GRPO (June 2, entropy-gated credit) and M-GRPO (June 2, momentum anchoring) by attacking a different failure mode: wasted rollout compute from uninformative groups rather than policy collapse.

## My Thoughts

<!-- Add your own notes here -->
