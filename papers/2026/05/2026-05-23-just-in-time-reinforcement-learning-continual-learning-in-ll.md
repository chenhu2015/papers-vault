---
title: "Just-In-Time Reinforcement Learning: Continual Learning in LLM Agents Without Gradient Updates"
authors: ["Yibo Li", "Zijie Lin", "Ailin Deng", "Xuan Zhang", "Yufei He", "Shuo Ji", "Tri Cao", "Bryan Hooi"]
date: 2026-05-23
arxiv_id: "2601.18510v1"
url: "http://arxiv.org/abs/2601.18510v1"
score: 0.78
topics: [agentic RL, LLM agent, RL training, reinforcement learning, RLHF]
status: unread
---

# Just-In-Time Reinforcement Learning: Continual Learning in LLM Agents Without Gradient Updates

## Summary

JitRL enables test-time policy optimization for LLM agents without any gradient updates: it maintains a non-parametric memory of past experiences, retrieves relevant trajectories to estimate action advantages on-the-fly, and directly modulates output logits using these estimates. The authors prove this additive update is the exact closed-form solution to the KL-constrained policy optimization objective. JitRL achieves state-of-the-art among training-free methods on WebArena and Jericho, outperforming expensive fine-tuning methods like WebRL while reducing cost by 30×.

## Key Contributions

- Gradient-free test-time RL: non-parametric memory + on-the-fly advantage estimation + logit modulation with no weight updates
- Theoretical proof that the logit-additive update is the closed-form KL-constrained policy optimization solution
- Addresses catastrophic forgetting and deployment-time adaptation simultaneously without retraining
- 30× cost reduction vs. WebRL fine-tuning while matching or exceeding its performance on WebArena and Jericho

## Relevance

A highly novel angle on agentic RL: instead of training the policy, JitRL performs RL inference-time through memory retrieval and logit modulation. This connects to the test-time compute / reasoning budget thread (sought for 3+ days) and to May 20's ICRL (internalized self-critique RL) from a complementary angle — JitRL externalizes policy improvement to memory rather than internalizing it.

## My Thoughts

<!-- Add your own notes here -->
