---
title: "From $P(y|x)$ to $P(y)$: Investigating Reinforcement Learning in Pre-train Space"
authors: ["Yuqiao Tan", "Minzheng Wang", "Bo Liu", "Zichen Liu"]
date: 2026-04-15
arxiv_id: "2604.14142"
url: "http://arxiv.org/abs/2604.14142v1"
score: 0.84
topics: [RL training, RLHF, reinforcement learning, agentic RL, GRPO]
status: unread
---

# From $P(y|x)$ to $P(y)$: Investigating Reinforcement Learning in Pre-train Space

## Summary

PreRL proposes applying RLVR to the marginal distribution P(y) in pre-train space rather than the conditional P(y|x), arguing that standard RLVR is fundamentally bounded by the base model's existing output distribution. The paper demonstrates strong gradient alignment between log P(y) and log P(y|x), enabling reward-driven online updates that encode reasoning ability while preserving broad exploration capacity beyond what post-training RLVR can achieve.

## Key Contributions

- Identifies the distribution ceiling of standard RLVR: bounded by base model's P(y|x)
- PreRL: reward-driven online updates applied to the marginal P(y) in pre-train space
- Theoretical and empirical proof of gradient alignment between log P(y) and log P(y|x)
- Demonstrates that reasoning ability can be encoded at the pretraining level, avoiding post-training constraints

## Relevance

This paper proposes a fundamentally different locus for RL training — at pretraining rather than fine-tuning time — which is a fresh angle not explored in the prior 10 days of digests. It directly addresses the ceiling problem of RLVR and connects to core interests in RL training and reasoning enhancement.

## My Thoughts

<!-- Add your own notes here -->
