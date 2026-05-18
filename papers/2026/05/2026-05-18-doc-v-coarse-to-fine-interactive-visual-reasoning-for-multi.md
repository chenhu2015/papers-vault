---
title: "Doc-V*:Coarse-to-Fine Interactive Visual Reasoning for Multi-Page Document VQA"
authors: ["Yuanlei Zheng", "Pei Fu", "Hang Li", "Ziyang Wang", "Yuyi Zhang", "Wenyu Ruan", "Xiaojin Zhang", "Zhongyu Wei", "Zhenbo Luo", "Jian Luan", "Wei Chen", "Xiang Bai"]
date: 2026-04-15
arxiv_id: "2604.13731v1"
url: "http://arxiv.org/abs/2604.13731v1"
score: 0.82
topics: [VLM, agentic RL, GRPO, multimodal, tool use, LLM agent]
status: unread
---

# Doc-V*:Coarse-to-Fine Interactive Visual Reasoning for Multi-Page Document VQA

## Summary

Doc-V* frames multi-page document VQA as sequential evidence aggregation with an OCR-free agentic VLM: a thumbnail overview triggers semantic retrieval → targeted page fetching → structured working memory for grounded reasoning. The agent is trained by imitation from expert trajectories then fine-tuned with GRPO, balancing answer accuracy with evidence-seeking efficiency. It achieves up to +47.9% over RAG baseline on out-of-domain benchmarks across five evaluation sets.

## Key Contributions

- OCR-free agentic design: thumbnail → semantic retrieval → targeted page fetching → structured working memory — replaces brittle passive retrieval with active navigation
- Two-stage training: imitation learning from expert trajectories, then GRPO optimization for joint accuracy + efficiency
- GRPO reward simultaneously optimizes answer correctness and evidence-seeking efficiency (not just final accuracy)
- +47.9% out-of-domain improvement over RAG baseline; selective attention rather than increased input pages drives gains

## Relevance

Applies GRPO-based agentic RL (core interest) to visual document understanding with active tool-like page navigation — combining the multi-turn agentic RL thread (May 16) with VLM and tool-use interest keywords. The coarse-to-fine evidence aggregation strategy is a distinct approach to long-horizon visual agent design compared to prior digest papers.

## My Thoughts

<!-- Add your own notes here -->
