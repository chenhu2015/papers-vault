---
title: "TIPS: Turn-Level Information-Potential Reward Shaping for Search-Augmented LLMs"
authors: ["Yutao Xie", "Nathaniel Thomas", "Nicklas Hansen", "Yang Fu", "Li Erran Li", "Xiaolong Wang"]
date: 2026-03-11
arxiv_id: "2603.22293v1"
url: "https://arxiv.org/abs/2603.22293"
score: 0.85
topics: [agentic RL, tool use, GRPO, PPO, LLM agent]
status: unread
---

# TIPS: Turn-Level Information-Potential Reward Shaping for Search-Augmented LLMs

## Summary

TIPS applies potential-based reward shaping at the turn level for multi-turn search-augmented LLMs: each reasoning+tool-call segment receives a dense reward based on the increased likelihood of the correct answer under a teacher model, overcoming the sparse/delayed reward problem in outcome-only RL. The potential-based formulation guarantees policy invariance while providing fine-grained per-turn guidance. TIPS outperforms GRPO/PPO baselines on 7 QA benchmarks by +11.8% EM and +13.6% F1 with Qwen-2.5 7B Instruct.

## Key Contributions

- Turn-level information-potential reward: each reasoning+search segment gets dense reward from teacher model confidence increase
- Potential-based formulation guarantees policy invariance (no bias introduced vs. original reward)
- Addresses unstable optimization from sparse/delayed rewards in multi-turn tool-use RL
- Consistent outperformance of both GRPO and PPO baselines across 7 diverse QA benchmarks

## Relevance

Connects directly to the dense reward / potential-based shaping thread (reward shaping explored in DVAO, May 26) and the multi-turn agentic tool-use RL thread, with a clean theoretical grounding in potential-based reward shaping that is absent from most empirical search-RL papers.

## My Thoughts

<!-- Add your own notes here -->
