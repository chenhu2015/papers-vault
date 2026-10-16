---
title: "rePIRL: Learn PRM with Inverse RL for LLM Reasoning"
authors: ["Xin Wu", "Kaijie Zhu", "Ying Zhang", "Lun Wang", "Wenbo Guo"]
date: 2026-10-16
arxiv_id: "2602.07832"
url: "https://arxiv.org/abs/2602.07832"
score: 0.78
topics: [reinforcement learning, reward model, RLAIF, RLHF]
status: unread
---

# rePIRL: Learn PRM with Inverse RL for LLM Reasoning

## Summary

rePIRL learns process reward models (PRMs) via an inverse RL-inspired dual cycle that alternates policy and PRM updates without requiring expert reward functions or suffering entropy collapse, and is shown to unify online and offline PRM learning methods under a single framework. Evaluated on math and coding reasoning, rePIRL outperforms existing PRM learning methods and provides beneficial signals for test-time training and test-time scaling. Customized techniques address the challenge of scaling traditional inverse RL to the vocabulary-space of LLMs.

## Key Contributions

- Dual learning cycle: policy and PRM updated interchangeably, requiring only an expert policy (not its reward function)
- Theoretical unification of online and offline PRM learning under the inverse RL framework
- Customized techniques to prevent entropy collapse when scaling inverse RL to LLM vocabulary spaces
- Shown to generalize to test-time training, test-time scaling, and early-signal identification for hard problems

## Relevance

rePIRL fills the "how do we learn a good PRM" gap that PROGRS and PASS both assume is solved. While those papers address how to use PRM scores in GRPO training, rePIRL addresses how to train the PRM itself from minimal assumptions — a prerequisite step directly upstream in the reward model pipeline.

## My Thoughts

<!-- Add your own notes here -->
