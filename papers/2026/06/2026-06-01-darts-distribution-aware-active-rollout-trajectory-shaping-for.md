---
title: "DARTS: Distribution-Aware Active Rollout Trajectory Shaping for Accelerating LLM Reinforcement Learning"
authors: ["Yujie Wang", "Siwei Chen", "Longzan Luo", "Xinyi Liu", "Xupeng Miao", "Fangcheng Fu", "Bin Cui"]
date: 2026-06-01
arxiv_id: "2605.30859"
url: "https://arxiv.org/abs/2605.30859"
score: 0.84
topics: [GRPO, PPO, LLM agent, RLHF]
status: unread
---

# DARTS: Distribution-Aware Active Rollout Trajectory Shaping for Accelerating LLM Reinforcement Learning

## Summary

DARTS targets the long-tail response length distribution in LLM RL rollouts — a root cause of efficiency bottlenecks — by actively shaping the distribution toward conciseness and certainty rather than just scheduling outlier prompts. A distribution-aware trajectory sampling mechanism selects from a redundant exploration space per prompt, and an adaptive redundancy allocation scheme maximizes shaping effectiveness and system throughput. Experiments show up to 1.77x acceleration over state-of-the-art systems without compromising model performance.

## Key Contributions

- Characterizes long-tail rollout inefficiency at finer intra-prompt granularity, identifying verbosity as the core source of overhead
- Active distribution shaping paradigm: reshape rollout distribution toward conciseness rather than filtering post-hoc
- Distribution-aware trajectory sampling from redundant exploration space, combined with adaptive redundancy allocation
- 1.77x system speedup over SOTA on LLM RL training without quality loss

## Relevance

RL training efficiency hasn't been directly targeted before in recent digests; DARTS addresses the practical scaling bottleneck of running GRPO/PPO at large scale. Complements EchoRL (today) which addresses a different training pathology (advantage degeneration vs. length-tail).

## My Thoughts

<!-- Add your own notes here -->
