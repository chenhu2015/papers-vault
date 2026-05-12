---
title: "Verifier-Free RL for LLMs via Intrinsic Gradient-Norm Reward"
authors: ["Xuexiang Wen", "Hang Yu", "Linchao Zhu", "Gaoang Wang"]
date: 2026-05-11
arxiv_id: "2605.09920v1"
url: "http://arxiv.org/abs/2605.09920v1"
score: 0.88
topics: [RLVR, RLAIF, reward model, RL training]
status: unread
---

# Verifier-Free RL for LLMs via Intrinsic Gradient-Norm Reward

## Summary

VIGOR proposes using the L2 norm of the policy's own teacher-forced gradients as an intrinsic reward signal for RLVR, completely eliminating dependence on gold labels or domain-specific verifiers. A √T length bias correction and group-wise rank shaping stabilize the reward signal across prompts; on Qwen2.5-7B trained only on math data, VIGOR achieves +3.31% average math accuracy and +1.91% code accuracy over RLIF baselines, demonstrating cross-domain transfer.

## Key Contributions

- Novel intrinsic reward: gradient norm of teacher-forced negative log-likelihood as a proxy for how well a completion aligns with the current policy
- √T length bias correction to eliminate systematic length confound in averaged token-level gradients
- Group-wise rank shaping to stabilize reward scales across diverse prompts
- Cross-domain transfer: math-only training yields code accuracy gains, suggesting the reward captures generalizable reasoning quality

## Relevance

VIGOR directly addresses the scalability bottleneck of RLVR—dependence on verifiable gold labels or domain-specific oracles—by proposing a self-referential intrinsic signal. This is a significant complement to VPR (also in today's digest), which takes the opposite approach of leaning into external symbolic oracles. Together the two papers frame the space of process reward alternatives.

## My Thoughts

<!-- Add your own notes here -->
