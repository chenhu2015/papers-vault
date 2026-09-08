---
title: "Trajectory-Relative Hindsight Distillation for Agentic Reinforcement Learning"
authors: ["Haoyu Zheng", "Yun Zhu", "Qing Wang", "Wenqiao Zhang"]
date: 2026-09-08
arxiv_id: "2608.07371v1"
url: "http://arxiv.org/abs/2608.07371v1"
score: 0.85
topics: [agentic RL, RL training, GRPO, reward model, LLM agent]
status: unread
---

# Trajectory-Relative Hindsight Distillation for Agentic Reinforcement Learning

## Summary

TRIAL introduces a turn-aligned scoring protocol for hindsight distillation in multi-turn agentic RL: for each decision turn it computes a signed log-probability gap between ordinary and hindsight-conditioned response distributions, then normalizes magnitudes jointly over the realized trajectory to produce allocation multipliers with unit mean. This redistributes dense supervision across turns without changing its average strength, outperforming GRPO across all 8 backbone/environment/metric combinations and improving WebShop success rate from 56.4% to 75.2% with Qwen3-1.7B.

## Key Contributions

- Turn-aligned scoring protocol: unified framework for allocating hindsight supervision across multi-turn trajectories
- Signed log-probability gap determines direction (which turns to up-weight vs. down-weight) and local strength from ordinary vs. hindsight-conditioned response comparison
- Trajectory-relative normalization: joint normalization over the realized trajectory with eligible-token-weighted unit mean, preserving total supervision budget
- Beats GRPO on all 8 benchmark combinations (2 backbones × 2 environments × 2 metrics); 75.2% WebShop (vs. 56.4% GRPO)

## Relevance

TRIAL extends the Sep 07 credit assignment thread via a structurally distinct hindsight-conditioning approach: unlike VICT (verifier-atom extraction), DiDPO (code-diff groupability anchors), or T-STAR (cognitive tree back-propagation), it derives credit signal by conditioning the model on realized consequences and measuring divergence from the non-hindsight response. The turn-aligned scoring protocol directly addresses the multi-turn credit weakness identified as a core challenge by RTPO, complementing RTPO's reverse-tree causal structure with a distribution-space alignment signal.

## My Thoughts

<!-- Add your own notes here -->
