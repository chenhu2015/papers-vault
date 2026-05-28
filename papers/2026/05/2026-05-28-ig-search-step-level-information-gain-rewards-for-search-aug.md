---
title: "IG-Search: Step-Level Information Gain Rewards for Search-Augmented Reasoning"
authors: ["Zihan Liang", "Yufei Ma", "Ben Chen", "Zhipeng Qian", "Huangyu Dai", "Lingtao Mao", "Xuxin Zhang", "Chenyi Lei", "Wenwu Ou"]
date: 2026-04-16
arxiv_id: "2604.15148v1"
url: "https://arxiv.org/abs/2604.15148"
score: 0.88
topics: [agentic RL, tool use, GRPO, LLM agent]
status: unread
---

# IG-Search: Step-Level Information Gain Rewards for Search-Augmented Reasoning

## Summary

IG-Search introduces step-level Information Gain (IG) rewards for search-augmented RL: each search step is scored by how much retrieved documents improve the model's confidence in the correct answer vs. a random-document counterfactual, then fed back to search-query tokens via per-token advantage modulation in GRPO. This enables fine-grained credit assignment without any intermediate annotations beyond standard QA pairs. On 7 QA benchmarks with Qwen2.5-3B, IG-Search achieves avg EM of 0.430, outperforming trajectory-level MR-Search by 1.6pp and step-level GiGPO by 0.9pp while adding only ~6.4% wall-clock overhead.

## Key Contributions

- Step-level IG reward measuring confidence improvement of retrieved docs vs. counterfactual random retrieval
- Per-token advantage modulation in GRPO for search-query tokens based on IG signal
- No intermediate annotations required — signal derived entirely from policy generation probabilities
- Formal analysis showing IG captures query effectiveness independent of trajectory randomness

## Relevance

Directly extends the search-augmented RL thread (PiCA, TIPS, EvalAct, SLATE all found this week) — IG-Search's counterfactual IG formulation is a clean orthogonal approach to step-level credit that requires zero extra supervision, making it especially interesting for the agentic RL + tool use angle in the interest profile.

## My Thoughts

<!-- Add your own notes here -->
