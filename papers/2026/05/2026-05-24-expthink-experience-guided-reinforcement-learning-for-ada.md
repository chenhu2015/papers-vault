---
title: "ExpThink: Experience-Guided Reinforcement Learning for Adaptive Chain-of-Thought Compression"
authors: ["Tingcheng Bian", "Yuzhe Zhang", "Jing Jin", "Jinchang Luo", "MingQuan Cheng", "Haiwei Wang", "Wenyuan Jiang", "Miaohui Wang"]
date: 2026-05-08
arxiv_id: "2605.07501v2"
url: "http://arxiv.org/abs/2605.07501v2"
score: 0.83
topics: [reinforcement learning, RL training, GRPO, reward model, RLHF]
status: unread
---

# ExpThink: Experience-Guided Reinforcement Learning for Adaptive Chain-of-Thought Compression

## Summary

ExpThink targets reasoning inefficiency in LRMs via two mechanisms: experience-guided reward shaping, which tracks the shortest correct solution seen so far per problem and tightens the threshold as the model improves (a self-evolving curriculum requiring no manual scheduling), and difficulty-adaptive advantage, which replaces standard-deviation normalization with correct-count normalization to scale gradients monotonically with difficulty. Together they enforce accuracy-first, compression-second learning. Across multiple math benchmarks, ExpThink reduces average response length by up to 77% while simultaneously improving accuracy, reaching 3× higher accuracy-efficiency ratio than the vanilla GRPO baseline.

## Key Contributions

- Experience-guided reward shaping: three-tier reward (full / discounted / zero) with self-tightening threshold based on per-problem shortest correct history
- Difficulty-adaptive advantage: correct-count normalization yields monotonically difficulty-scaled gradients, preserving accuracy on hard problems while encouraging brevity on easy ones
- No manual curriculum scheduling—curriculum emerges from model's own improving capability
- Consistent outperformance of existing RL-based CoT compression methods on both accuracy and length metrics

## Relevance

Fills the reasoning-budget RL gap that eluded 3 consecutive search attempts (May 21–23); unlike CLORE (May 23, content-level editing) and LamPO (May 23, advantage topology), ExpThink operates at the reward-shaping level with a self-evolving difficulty signal—a distinct and complementary angle.

## My Thoughts

<!-- Add your own notes here -->
