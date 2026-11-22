---
title: "Anti-Length Shift: Dynamic Outlier Truncation for Training Efficient Reasoning Models"
authors: ["Wei Wu", "Liyi Chen", "Congxi Xiao", "Tianfu Wang", "Qimeng Wang", "Chengqiang Lu", "Yan Gao", "Yi Wu", "Yao Hu", "Hui Xiong"]
date: 2026-01-07
arxiv_id: "2601.03969"
url: "https://arxiv.org/abs/2601.03969"
score: 0.80
topics: [RL training, GRPO, agentic RL, reward model]
status: unread
---

# Anti-Length Shift: Dynamic Outlier Truncation for Training Efficient Reasoning Models

## Summary

Anti-Length Shift introduces Dynamic Outlier Truncation (DOT), a training-time intervention targeting 'length shift' — the tendency of RLVR-trained models to become increasingly verbose on simple queries. DOT selectively suppresses redundant tokens only in the extreme tail of response lengths within fully-correct rollout groups, combined with auxiliary KL regularization and predictive dynamic sampling for stable convergence. Applied during GRPO training, it reduces inference token usage by 78% on AIME-24 while simultaneously improving accuracy over the initial policy, pushing the efficiency-performance Pareto frontier outward.

## Key Contributions

- Identifies "length shift" as a distinct failure mode of RLVR training: models increasingly over-generate on simple inputs during the training process
- Dynamic Outlier Truncation (DOT): targets only the extreme tail of response lengths within fully-correct rollout groups, avoiding interference with complex reasoning chains
- Auxiliary KL regularization + predictive dynamic sampling to maintain stable convergence during the truncation intervention
- 78% inference token reduction on AIME-24 with simultaneous accuracy improvement over the initial policy

## Relevance

Directly extends the adaptive reasoning RL cluster (TON, ThinkWise, DR-BOLT, Omni-AutoThink) with an orthogonal training-time mechanism: unlike TON's binary think/not-think gate or ThinkWise's perception-conditioned length regulation, DOT intervenes at the response-length distribution level during RLVR training without modifying the policy objective. Follows the TON-adjacent budget control probe from the Nov 21 digest.

## My Thoughts

<!-- Add your own notes here -->
