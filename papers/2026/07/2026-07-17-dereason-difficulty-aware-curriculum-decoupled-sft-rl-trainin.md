---
title: "DeReason: A Difficulty-Aware Curriculum Improves Decoupled SFT-then-RL Training for General Reasoning"
authors: ["Hanxu Hu", "Yuxuan Wang", "Maggie Huan", "Jannis Vamvas", "Yinya Huang", "Zhijiang Guo", "Rico Sennrich"]
date: 2026-07-17
arxiv_id: "2603.11193v1"
url: "http://arxiv.org/abs/2603.11193v1"
score: 0.82
topics: [RL training, reinforcement learning, GRPO]
status: unread
---

# DeReason: A Difficulty-Aware Curriculum Improves Decoupled SFT-then-RL Training for General Reasoning

## Summary

Reveals that for general STEM domains, direct RL on base models is highly sample-inefficient and consistently surpassed by SFT alone, yet sequential SFT→RL yields further gains — confirming the two stages are complementary. DeReason proposes difficulty-based data decoupling via LLM-based scoring: non-reasoning-intensive problems are allocated to SFT for foundational domain knowledge, while reasoning-intensive problems are reserved for RL to cultivate complex reasoning. Outperforms random-split SFT→RL and SFT-only baselines on general STEM and math benchmarks.

## Key Contributions

- Controlled experiments showing RL on base models is sample-inefficient for STEM; SFT alone outperforms raw RL but SFT→RL further improves
- Difficulty-based data decoupling via LLM-based reasoning intensity scoring into two complementary subsets
- Non-reasoning-intensive → SFT (broad domain coverage); reasoning-intensive → RL (focused complex reasoning)
- Outperforms both random-split SFT→RL and SFT-only baselines on general STEM and math benchmarks

## Relevance

The vault has tracked the SFT→RL two-stage design as an emerging pattern across agentic RL papers (TTI, RSPO, VRRL, Learning When to Plan, TurnOPD). DeReason is the most principled treatment of *why* the split matters: it shows empirically that the two stages serve distinct functions and that naive data splitting underperforms difficulty-aware partitioning. Directly extends the SFT→RL thread from math to general STEM.

## My Thoughts

<!-- Add your own notes here -->
