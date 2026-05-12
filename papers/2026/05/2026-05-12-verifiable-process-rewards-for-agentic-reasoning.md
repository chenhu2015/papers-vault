---
title: "Verifiable Process Rewards for Agentic Reasoning"
authors: ["Huining Yuan", "Zelai Xu", "Huaijie Wang", "Xiangmin Yi", "Jiaxuan Gao", "Xiao-Ping Zhang", "Yu Wang", "Chao Yu", "Yi Wu"]
date: 2026-05-11
arxiv_id: "2605.10325v1"
url: "http://arxiv.org/abs/2605.10325v1"
score: 0.92
topics: [agentic RL, reward model, RL training, LLM agent, agentic]
status: unread
---

# Verifiable Process Rewards for Agentic Reasoning

## Summary

VPR proposes converting symbolic and algorithmic oracles into dense turn-level process rewards for RL in long-horizon agentic tasks, addressing the credit assignment problem caused by sparse outcome-only feedback. The framework is instantiated across three verification paradigms—search-based deduction, constraint-based logical reasoning, and posterior-based probabilistic inference—and provides theoretical analysis showing dense verifier-grounded rewards improve learning signal locality over outcome-level rewards. Empirically, VPR outperforms outcome-level and rollout-based PRM baselines and transfers to general reasoning benchmarks.

## Key Contributions

- Formally defines Verifiable Process Rewards (VPR) as a framework for converting symbolic/algorithmic oracles into dense turn-level RL supervision
- Instantiates VPR in three agentic reasoning domains: search-based deduction, constraint-based logical reasoning, and posterior-based probabilistic inference
- Theoretical analysis proving that dense verifier-grounded rewards improve long-horizon credit assignment compared to sparse outcome-level rewards, with benefit depending on oracle reliability
- Empirical transfer to both general and agentic reasoning benchmarks beyond training environments

## Relevance

This paper directly addresses the core credit assignment challenge in agentic RL—how to provide informative step-level signals without outcome-only rewards—by grounding process rewards in verifiable symbolic oracles rather than learned models. This is a key gap in the PRM training thread that Search 3 was probing today.

## My Thoughts

<!-- Add your own notes here -->
