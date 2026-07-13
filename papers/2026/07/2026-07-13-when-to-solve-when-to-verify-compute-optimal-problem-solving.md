---
title: "When To Solve, When To Verify: Compute-Optimal Problem Solving and Generative Verification for LLM Reasoning"
authors: ["Nishad Singhi", "Hritik Bansal", "Arian Hosseini", "Aditya Grover", "Kai-Wei Chang", "Marcus Rohrbach", "Anna Rohrbach"]
date: 2026-07-13
arxiv_id: "2504.01005v2"
url: "https://arxiv.org/abs/2504.01005"
score: 0.80
topics: [RL training, reward model, agentic RL, RLHF]
status: unread
---

# When To Solve, When To Verify: Compute-Optimal Problem Solving and Generative Verification for LLM Reasoning

## Summary

A compute-budget analysis of GenRM (Generative Reward Model) versus Self-Consistency (SC) under fixed inference budgets. SC is more compute-efficient than GenRM for most practical budgets — GenRM only matches SC after consuming 8x the inference compute. Derived inference scaling laws show that compute-optimal inference favors scaling solution generation more aggressively than the number of verifications. This characterizes the regime in which RL^V-style co-trained generative verifiers become worthwhile.

## Key Contributions

- GenRM requires 8x the inference compute to first match SC; requires significantly more to outperform it — SC is the practical default at most inference budgets
- Inference scaling laws for the GenRM paradigm: scale solutions faster than verification count for compute-optimal inference
- Comprehensive evaluation across diverse models and datasets, showing the SC-vs-GenRM trade-off is consistent
- Practical guidance: compute-optimal allocation favors aggressive solution generation scaling before investing in per-solution verification

## Relevance

Characterizes the inference-time compute regime where RL^V's ([[2026-07-12-putting-the-value-back-in-rl-better-test-time-scaling-by-un]]) generative verifier becomes worthwhile: only at 8x+ compute overhead relative to SC. This reframes T1's ([[2026-07-12-t1-advancing-language-model-reasoning-through-reinforcement]]) oversampling diversity result: T1 trains models to benefit from scaling solutions (the dominant side of the trade-off per this paper); RL^V provides the verifier for the regime where verification cost is justifiable. Together with Tango ([[2026-07-13-rl-tango-reinforcing-generator-and-verifier-together-for-la]]), these three papers form the complete compute-allocation picture: train solutions to be diverse (T1), co-train a verifier to select (Tango/RL^V), deploy verifier only above 8x budget (this paper).

## My Thoughts

<!-- Add your own notes here -->
