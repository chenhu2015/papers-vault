---
title: "Learning When to Think: Dual-Reference Offline Optimization for Adaptive VLM Reasoning"
authors: ["Hongbin Lin", "Sizhe Zou", "Juangui Xu", "Xinyue Xu", "Zhuoli Ouyang", "Stanislav Kolchin", "Chengwei Qin", "Zhongxiang Dai", "Yao Shu"]
date: 2026-11-06
arxiv_id: "2611.09154v2"
url: "http://arxiv.org/abs/2611.09154v2"
score: 0.75
topics: [VLM, vision-language models, multimodal models, agentic RL, GRPO]
status: unread
---

# Learning When to Think: Dual-Reference Offline Optimization for Adaptive VLM Reasoning

## Summary

DR-BOLT proposes a dual-reference offline optimization that corrects the mismatch between the fast/slow thinking mixture target distribution and the sampling distribution in adaptive VLM reasoning, with source-wise correction for well-separated response formats. Achieves a 2.90× training speedup over GRPO while improving score-length trade-offs on ScienceQA and three held-out transfer benchmarks, with 24.1% cross-benchmark slow ratio.

## Key Contributions

- Dual-reference formulation: explicitly separates the desired fast/slow mixture reference from the data-generating sampling distribution, correcting their mismatch
- Source-wise correction approximates the exact objective efficiently when fast/slow formats are well-separated
- 2.90× training speedup over online GRPO with competitive or better score-length trade-offs
- Demonstrates transfer across distribution: fast/slow routing generalizes to held-out benchmarks without retraining

## Relevance

Offline counterpart to APMPO/GRPO objective work: DR-BOLT modifies the reference distribution rather than the update aggregation rule. The dual-reference formulation relates to EPIC's exact prefix IS ratio and LGPO's on-policy ratio, but applied to the routing decision in adaptive reasoning — a new angle in the GRPO objective variants cluster.

## My Thoughts

<!-- Add your own notes here -->
