---
title: "Understanding and Mitigating Spurious Signal Amplification in Test-Time Reinforcement Learning for Math Reasoning"
authors: ["Yongcan Yu", "Lingxiao He", "Jian Liang", "Kuangpu Guo", "Meng Wang", "Qianlong Xie", "Xingxing Wang", "Ran He"]
date: 2026-05-14
arxiv_id: "2604.21327"
url: "https://arxiv.org/abs/2604.21327"
score: 0.84
topics: [GRPO, PPO, RL training, RLHF, reward model]
status: unread
---

# Understanding and Mitigating Spurious Signal Amplification in Test-Time Reinforcement Learning for Math Reasoning

## Summary

Test-time RL (TTRL) adapts models via pseudo-labels, which introduces label noise; GRPO's group-relative advantage estimation further amplifies these spurious signals through medium-consistency ambiguous samples. DDRL mitigates this with three components: frequency-based sampling that excludes ambiguous samples while keeping balanced positive/negative sets, fixed advantages replacing GRPO's relative ones to remove bias, and consensus-based off-policy refinement for efficient stable updates. DDRL consistently outperforms existing TTRL baselines across multiple LLMs and math benchmarks.

## Key Contributions

- Identifies medium-consistency ambiguous samples as the primary source of reward noise in TTRL
- Proves that GRPO's group-relative advantage estimation amplifies spurious signals (not just passes them through)
- Frequency-based sampling excludes the ambiguity region while maintaining balanced reward signal
- Fixed advantages replace GRPO's relative ones, eliminating the statistical bias introduced by group normalisation

## Relevance

Connects to the iterative RLHF collapse thread (Alignment Collapse from May 12) and the reward hacking analysis (May 11). This is the test-time analogue: where standard RLHF training uses external reward models, TTRL uses pseudo-labels — but the failure mode (spurious signal amplification via GRPO) is a shared structural property worth understanding.

## My Thoughts

<!-- Add your own notes here -->
