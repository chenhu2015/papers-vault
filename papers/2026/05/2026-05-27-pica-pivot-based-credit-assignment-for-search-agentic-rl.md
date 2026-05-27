---
title: "PiCA: Pivot-Based Credit Assignment for Search Agentic Reinforcement Learning"
authors: ["Dongyi Liu", "Yifan Niu", "Qinwen Wang", "Han Xiao", "Jia Li"]
date: 2026-05-27
arxiv_id: "2605.09287v2"
url: "http://arxiv.org/abs/2605.09287v2"
score: 0.87
topics: [agentic RL, LLM agent, RL training, reward model, tool use]
status: unread
---

# PiCA: Pivot-Based Credit Assignment for Search Agentic Reinforcement Learning

## Summary

PiCA defines step rewards for search agents using Potential-Based Reward Shaping anchored to pivot steps — critical golden sub-queries and sub-answers that significantly boost the likelihood of a correct final answer. Process rewards are formulated as context-dependent success probabilities, providing dense, trajectory-aware credit while maintaining distributional consistency with the model's natural generation distribution. Achieves +15.2%/+2.2% on 3B/7B models across 7 knowledge-intensive QA benchmarks.

## Key Contributions

- Addresses three long-horizon credit assignment failures: reward sparsity, isolated credit, distributional shift
- Pivot identification: golden sub-queries/sub-answers mined from historical trajectories as information peaks
- PBRS-based step rewards: context-dependent success probabilities anchored to pivot steps
- Distributional consistency maintained by anchoring rewards to the model's natural generative process

## Relevance

Directly addresses the search-agent RL angle (today's query 4 theme) with a principled credit assignment solution. Connects to the HyperEyes (May 23) and InfoTree (May 24) threads on efficient tool-use RL; PiCA's pivot mechanism is a cleaner, PBRS-grounded alternative to those approaches.

## My Thoughts

<!-- Add your own notes here -->
