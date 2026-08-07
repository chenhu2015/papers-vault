---
title: "Beyond the Mean: Multi-Moment Policy Optimization for LLM Reasoning"
authors: ["Yijun Zhang", "Yule Xie", "Jiaxin Ding", "Xin Ding"]
date: 2026-08-03
arxiv_id: "2608.02149v1"
url: "https://arxiv.org/abs/2608.02149"
score: 0.77
topics: [reinforcement learning, RLHF, GRPO, reward model]
status: unread
---

# Beyond the Mean: Multi-Moment Policy Optimization for LLM Reasoning

## Summary

MMPO frames LLM RL objectives by treating each problem's failure probability as a random variable and optimizing via its statistical moments. Existing methods (GRPO and variants) optimize only the mean (first moment); MMPO jointly minimizes multiple moments (mean, variance, skewness), admitting an operational interpretation as minimizing the expected truncated time to first success. A general moment-transformation framework provides a unified view of the broader family of policy optimization objectives, consistently outperforming strong baselines across five math reasoning benchmarks.

## Key Contributions

- Moment-based perspective: failure probability of a sampled problem treated as a random variable; optimization over its distribution rather than expectation alone
- MMPO jointly minimizes multiple moments (mean, variance, skewness) — operational interpretation: minimize expected truncated time to first successful response
- General moment-transformation framework that subsumes GRPO and related methods as special cases optimizing a single moment
- Consistent outperformance of strong baselines across 5 math benchmarks at multiple model scales

## Relevance

MMPO provides a theoretical unification of the GRPO family from the moment perspective, directly connecting to Dark Room (Aug 6), which showed z-score normalization cancels dense shaping in all-fail groups (a structural failure of mean-only optimization). MMPO's moment-transformation framework extends this: GOPO's ordinal ranking (Aug 3) is a special case of reward transformation; MMPO's variance and skewness terms explicitly counteract the instability that Dark Room attributed to all-fail group z-score cancellation. This closes a theoretical gap in the vault's Gap #16 synthesis — the formal unifying lens for why all-fail group handling methods work is now: they reduce higher moments of the failure-probability distribution that standard GRPO leaves uncontrolled.

## My Thoughts

<!-- Add your own notes here -->
