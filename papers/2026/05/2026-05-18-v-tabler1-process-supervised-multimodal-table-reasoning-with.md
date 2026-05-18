---
title: "V-tableR1: Process-Supervised Multimodal Table Reasoning with Critic-Guided Policy Optimization"
authors: ["Yubo Jiang", "Yitong An", "Xin Yang", "Abudukelimu Wuerkaixi", "Xuxin Cheng", "Fengying Xie", "Zhiguo Jiang", "Cao Liu", "Ke Zeng", "Haopeng Zhang"]
date: 2026-04-22
arxiv_id: "2604.20755v1"
url: "http://arxiv.org/abs/2604.20755v1"
score: 0.88
topics: [VLM, reward model, RL training, multimodal, GRPO, agentic RL]
status: unread
---

# V-tableR1: Process-Supervised Multimodal Table Reasoning with Critic-Guided Policy Optimization

## Summary

V-tableR1 trains multimodal LLMs to reason verifiably over structured tables using a critic VLM that provides dense step-level feedback on visual chain-of-thought. The PGPO algorithm (Process-Guided Direct Alignment Policy Optimization) integrates these process rewards with decoupled policy constraints and length-aware dynamic sampling, extending RLVR to visual domains where binary outcome rewards produce black-box reasoning. A 4B V-tableR1 achieves state-of-the-art on complex tabular benchmarks, outperforming models up to 18× its size and improving over its SFT baseline.

## Key Contributions

- PGPO: novel RL algorithm combining process rewards from a critic VLM, decoupled policy constraints (separate KL penalties per step), and length-aware dynamic sampling
- Identifies that RLVR with only outcome rewards causes "visual hallucinations and shortcut guessing" in multimodal table reasoning — process supervision is the fix
- 4B model beats open-source models up to 72B on complex tabular benchmarks
- Shifts multimodal inference from black-box pattern matching to verifiable logical derivation

## Relevance

Directly extends the GRPO/RLVR training paradigm (core interest) into the VLM+structured visual reasoning domain, using a critic VLM as a process reward model — combining two core interest profile threads (reward model + VLM). Adds a new data point to the query 4 (structured visual RL) thread uncovered today.

## My Thoughts

<!-- Add your own notes here -->
