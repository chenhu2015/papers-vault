---
title: "Turning Off-Policy Tokens On-Policy: A Plug-in Approach for Improving LLM Alignment"
authors: ["Yu Li", "Xiuyu Li", "Mingyang Yi", "Jiaxing Wang", "zhangliangxu", "Zhaolong Xing", "Zhen Chen"]
date: 2026-07-06
arxiv_id: "2607.04728"
url: "https://arxiv.org/abs/2607.04728"
score: 0.77
topics: [RLHF, RL training, LLM agent, PPO]
status: unread
---

# Turning Off-Policy Tokens On-Policy: A Plug-in Approach for Improving LLM Alignment

## Summary

Selective Importance Sampling (SIS) addresses the fundamental off-policy mismatch in LLM RL post-training by implementing token-level rejection sampling: treating the off-policy model as a proposal distribution, each token is either accepted (unit importance weight, treated as on-policy) or rejected (retaining standard IS correction). SIS is proved to reduce the gap between token-level and sequence-level off-policy gradient estimators, adds negligible overhead as a plug-in IS ratio modification, and consistently improves math and agent benchmarks across dense and MoE LLMs.

## Key Contributions

- **Token-level rejection test**: off-policy model as proposal distribution; accepted tokens get unit IS weight (on-policy treatment); rejected tokens retain standard IS correction
- **Theoretical guarantee**: SIS provably reduces the gap between token-level and sequence-level off-policy gradient estimators, addressing IS variance explosion from compounding token-level ratios
- **Plug-in design**: only modifies IS ratio in policy loss, no architecture changes, negligible wall-clock overhead
- **Dense and MoE LLM improvements** on math and agent benchmarks, robust to off-policy data degree

## Relevance

Complementary mechanism to ARMOR (Jul 28, off-policy anchor rollouts for on-policy stability): ARMOR prevents over-optimization by mixing in reference-policy anchor data; SIS addresses the same off-policy data problem from the IS correction angle — selectively accepting tokens rather than mixing in separate anchor trajectories. Together they form two sides of the off-policy data integration problem: ARMOR (what data to mix in) and SIS (how to weight mixed/off-policy tokens). SIS is also relevant to OC-GRPO (today, IS-corrected guided rollouts) as both use IS to bridge off-policy → on-policy objectives.

## My Thoughts

<!-- Add your own notes here -->
