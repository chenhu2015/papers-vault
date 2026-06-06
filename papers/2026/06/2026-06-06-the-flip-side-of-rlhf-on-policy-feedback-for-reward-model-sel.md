---
title: "The Flip Side of RLHF: On-Policy Feedback for Reward Model Self-Supervised Improvement"
authors: ["Xiaobo Wang", "Tong Wu", "Min Tang", "Jiaqi Li", "Qi Liu", "Zilong Zheng"]
date: 2026-06-06
arxiv_id: "2605.30888v1"
url: "http://arxiv.org/abs/2605.30888v1"
score: 0.82
topics: [RLHF, reward model, RL training, GRPO, reinforcement learning]
status: unread
---

# The Flip Side of RLHF: On-Policy Feedback for Reward Model Self-Supervised Improvement

## Summary

SAVE (Self-supervised reward model improvement via Value-Anchored On-policy feedback) uses a prompt-specific value head as an adaptive anchor to grade on-policy responses, converting them into self-supervised RM training signal without additional human annotation. RM advantages are computed and ambiguous samples filtered via a contrastive objective, allowing the reward model to stay in sync with a changing policy distribution. SAVE consistently outperforms static RM baselines across six benchmarks and is compatible with GRPO, RLOO, and GSPO training algorithms.

## Key Contributions

- Identifies the core problem: static reward models degrade as the policy evolves past their training distribution
- Prompt-specific value head provides adaptive anchor for grading on-policy responses self-supervisedly
- Contrastive objective with ambiguity filtering converts value-graded responses into clean RM training signal
- Validated across 6 benchmarks and 3 RL algorithms (GRPO, RLOO, GSPO), with consistent improvement over static RM baselines

## Relevance

SAVE addresses the reward model distributional mismatch problem from an angle not yet covered in the digest — self-supervised online RM adaptation. This complements the Reward Bias Substitution paper (May 31) which identified the structural failure mode, and RLAR (today) which handles it via dynamic tool synthesis. SAVE is the most practical solution for standard RLHF pipelines.

## My Thoughts

<!-- Add your own notes here -->
