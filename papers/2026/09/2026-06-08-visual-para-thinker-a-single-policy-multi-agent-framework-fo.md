---
title: "Visual Para-Thinker++: A Single-Policy Multi-Agent Framework for Visual Reasoning"
authors: ["Haoran Xu", "Hongyu Wang", "Yifei Gao", "Jiaze Li", "Zizhao Tong", "Xiaofeng Zhang", "Xiaosong Yuan"]
date: 2026-06-08
arxiv_id: "2606.09290v1"
url: "http://arxiv.org/abs/2606.09290v1"
score: 0.80
topics: [multimodal models, vision language models, agentic RL, VLM, LLM agent]
status: unread
---

# Visual Para-Thinker++: A Single-Policy Multi-Agent Framework for Visual Reasoning

## Summary

Visual Para-Thinker++ instantiates one shared MLLM policy as role-conditioned Main, Worker, and Summary Agents. Role-Decoupled Multi-Agent Optimization assigns role-specific rewards and advantages to corresponding token segments, reducing gradient conflict among collaborative roles; KV cache reuse enables efficient multi-agent rollout. On V*, CountBench, RefCOCO, and HallusionBench, the framework consistently outperforms single-trajectory and inference-time parallel baselines, with especially strong gains on hallucination-sensitive tasks.

## Key Contributions

- Single-policy multi-agent architecture: one MLLM policy instantiated as three role-conditioned agents — Main (task decomposition), Workers (parallel reasoning under context isolation), Summary (reconciles full reasoning traces)
- Role-Decoupled Multi-Agent Optimization: assigns role-specific rewards and advantages to corresponding token segments, preventing gradient conflict between roles that have different objectives
- Summary Agent reconciles full Worker reasoning traces rather than majority-voting on final labels — avoids losing nuance in aggregation
- KV cache reuse across role instances enables efficient multi-agent rollout; visual prefix shared across Workers

## Relevance

Visual Para-Thinker++ bridges two threads: the multi-agent harness optimization work (ScienceBuddy Sep 16, Ecdysis Sep 11, EvoHarness Sep 7) and the VLM RL training gap (ReVisual-R1 Sep 16, MSRL Sep 5). The role-decoupled advantage assignment is directly analogous to the FACTOR credit-conserving token-level credit in multi-turn agents but applied to role boundaries rather than turn boundaries; comparing the two decompositions is an open empirical question. The hallucination-sensitive gains suggest that context isolation among Workers is doing work beyond just parallelism.

## My Thoughts

<!-- Add your own notes here -->
