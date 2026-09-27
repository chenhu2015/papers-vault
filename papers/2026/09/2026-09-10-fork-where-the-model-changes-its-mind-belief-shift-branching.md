---
title: "Fork Where the Model Changes Its Mind: Belief-Shift Branching for Tree-Structured Reinforcement Learning"
authors: ["Bin Lei", "Yu Li", "Prafulla Kumar Choubey", "Jiaxin Zhang", "Becky Xiangyu Peng", "Qinyuan Ye", "Kartik Narayan", "Caiwen Ding", "Silvio Savarese", "Chien-Sheng Wu"]
date: 2026-09-10
arxiv_id: "2609.11061v1"
url: "http://arxiv.org/abs/2609.11061v1"
score: 0.87
topics: [agentic RL, RL training, reinforcement learning, GRPO]
status: unread
---

# Fork Where the Model Changes Its Mind: Belief-Shift Branching for Tree-Structured Reinforcement Learning

## Summary

Belief-Shift Branching formalizes tree fork placement as locating value-curve pivots — points where the model's answer belief shifts most between adjacent boundaries — rather than using fixed-length or entropy-based placement. Three instantiations (black-box probe, logit-lens depth profile, learned activation direction) place forks with ~1% overhead on math and ~5% on code, without requiring step-level supervision. Against Monte-Carlo value curves across eight model×benchmark panels, belief-shift ranking leads all baselines; in RL training, OLMo-3-7B gains +2.6 aggregate on math and +6.5 on LiveCodeBench-medium over the strongest baseline.

## Key Contributions

- Pivot formalization: fork placement = locating where expected outcome turns, not where entropy is high
- Three access-level instantiations: black-box probe (no internals), logit-lens depth profile, learned offline activation direction (~1% compute overhead)
- Belief-shift signal is fit offline before RL training — not a running per-step cost during rollout
- Demonstrates that next-token entropy is a poor proxy for value-curve pivots (outperformed in all 8 panels)

## Relevance

Direct complement to EPIG-Tree (2026-09-17), which derives optimal branching from law-of-total-variance decomposition. EPIG-Tree tells you *how many* branches to allocate; Belief-Shift Branching tells you *where* to place them. Together they form a principled tree rollout design space that was previously heuristic-driven.

## My Thoughts

<!-- Add your own notes here -->
