---
title: "The Optimal Token Baseline: Variance Reduction for Long-Horizon LLM-RL"
authors: ["Yingru Li", "Jiawei Xu", "Ziniu Li", "Jiacai Liu", "Wei Liu", "Yuxuan Tong", "Longtao Zheng", "Zhenghai Xue", "Yaxiang Zhang", "Tianle Cai", "Ge Zhang", "Qian Liu", "Baoxiang Wang"]
date: 2026-02-06
arxiv_id: "2602.07078"
url: "https://arxiv.org/abs/2602.07078"
score: 0.87
topics: [RL training, GRPO, PPO, agentic RL, reward model]
status: unread
---

# The Optimal Token Baseline: Variance Reduction for Long-Horizon LLM-RL

## Summary

The Optimal Token Baseline (OTB) derives a provably variance-minimizing token-level baseline for LLM RL by weighting gradient updates inversely proportional to their cumulative gradient norm. An efficient Logit-Gradient Proxy approximates the exact baseline from forward-pass probabilities alone, avoiding expensive backward computation. OTB matches training stability of group size N=32 with N=4, cutting token consumption by over 65% across single-turn and tool-integrated reasoning tasks.

## Key Contributions

- Optimal Token Baseline theorem: proves gradient updates should be weighted inversely by cumulative gradient norm to achieve global variance reduction
- Logit-Gradient Proxy: approximates gradient norm using only forward-pass token probabilities — no backward pass required
- Matches N=32 group-size training stability with N=4, reducing token consumption by 65%+
- Applies to both single-turn and tool-integrated long-horizon agentic reasoning tasks

## Relevance

OTB directly extends the advantage estimation thread opened by MaxPO (Aug 31) — MaxPO proves GRPO's group-based advantages are non-centered (non-zero batch sum) and proposes L2O centering; OTB proves that group-based baselines further overlook within-sequence token heterogeneity and proposes an optimal per-token weighting. Together, MaxPO L2O centering + OTB token weighting constitute a two-axis improvement plan for GRPO-style training: fix centering and fix per-token variance simultaneously.

## My Thoughts

<!-- Add your own notes here -->
