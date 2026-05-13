---
title: "Step-KTO: Optimizing Mathematical Reasoning through Stepwise Binary Feedback"
authors: ["Yen-Ting Lin", "Di Jin", "Tengyu Xu", "Tianhao Wu", "Sainbayar Sukhbaatar", "Chen Zhu", "Yun He", "Yun-Nung Chen", "Jason Weston", "Yuandong Tian", "Arash Rahnama", "Sinong Wang", "Hao Ma", "Han Fang"]
date: 2025-01-18
arxiv_id: "2501.10799v1"
url: "http://arxiv.org/abs/2501.10799v1"
score: 0.83
topics: [RLHF, reward model, RL training, reinforcement learning]
status: unread
---

# Step-KTO: Optimizing Mathematical Reasoning through Stepwise Binary Feedback

## Summary

Step-KTO extends the KTO alignment framework to mathematical reasoning by providing binary correctness signals at both individual reasoning steps (process reward) and the final answer, encouraging LLMs to follow logically coherent trajectories rather than exploit shortcuts. Unlike PPO or DPO, it requires only binary desirability labels — no pairwise preferences — at each step, and significantly improves Pass@1 accuracy on MATH-500 over strong baselines while improving intermediate step quality.

## Key Contributions

- Combines process-level and outcome-level binary feedback under the KTO loss (no pairwise comparisons needed)
- Step-level binary evaluator assigns binary correctness to intermediate reasoning steps
- Encourages adherence to logical progression rather than shortcut heuristics
- Significant Pass@1 improvement on MATH-500 over strong baselines
- Improves both final answer accuracy and intermediate step coherence simultaneously

## Relevance

Bridges two core profile threads: KTO (a RLHF alternative never previously surfaced in 12 days of digests) and process reward models (PRMs; heavily covered in digests like VPR/VIGOR/LEAD on May 12). Step-KTO uniquely combines both by applying KTO-style binary alignment at the step level — a synthesis not yet seen in the digest.

## My Thoughts

<!-- Add your own notes here -->
