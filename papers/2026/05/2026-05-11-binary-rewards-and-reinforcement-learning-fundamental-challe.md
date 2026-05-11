---
title: "Binary Rewards and Reinforcement Learning: Fundamental Challenges"
authors: ["Marc Dymetman"]
date: 2026-05-04
arxiv_id: "2605.02375"
url: "http://arxiv.org/abs/2605.02375v1"
score: 0.88
topics: [RLHF, GRPO, PPO, RL training, reward model, reinforcement learning]
status: unread
---

# Binary Rewards and Reinforcement Learning: Fundamental Challenges

## Summary

This paper provides a structural theoretical account of diversity collapse in RLVR: binary rewards create a fundamental degeneracy where infinitely many distributions maximize expected reward, giving policy gradient methods no principled selection criterion. KL-control (as used in PPO/GRPO regularization) resolves this by selecting the entropy-maximizing reward-satisfying distribution, explaining why removing the KL penalty causes the observed collapse in multi-sample coverage.

## Key Contributions

- Formal proof that binary rewards create distributional degeneracy for policy gradient
- Theoretical explanation of the diversity collapse (pass@1 improves, pass@k degrades) observed in RLVR
- KL-control shown to resolve degeneracy by imposing an entropy-maximizing selection principle
- Connects empirical GRPO/PPO regularization practice to theoretical necessity

## Relevance

This is a direct theoretical contribution to understanding why GRPO/PPO with verifiable rewards behaves the way it does — a gap in the prior 10 days of digests, which covered algorithmic variants without addressing the underlying theory. The diversity collapse analysis is highly relevant to practical RLVR training.

## My Thoughts

<!-- Add your own notes here -->
