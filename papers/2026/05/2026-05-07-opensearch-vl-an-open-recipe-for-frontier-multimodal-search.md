---
title: "OpenSearch-VL: An Open Recipe for Frontier Multimodal Search Agents"
authors: ["Shuang Chen", "Kaituo Feng", "Hangting Chen", "Wenxuan Huang", "Dasen Dai", "Quanxin Shou", "Yunlong Lin", "Xiangyu Yue", "Shenghua Gao", "Tianyu Pang"]
date: 2026-05-06
arxiv_id: "2605.05185"
url: "https://arxiv.org/abs/2605.05185"
score: 0.85
topics: [agentic RL, VLM, multimodal, GRPO, tool use, vision-language]
status: unread
---

# OpenSearch-VL: An Open Recipe for Frontier Multimodal Search Agents

## Summary

OpenSearch-VL provides a fully open-source recipe for training multimodal deep search agents via agentic RL: a data-curation pipeline (Wikipedia path sampling, fuzzy entity rewriting, source-anchor visual grounding) produces SearchVL-SFT-36k and SearchVL-RL-8k, paired with a diverse 7-tool environment. A multi-turn fatal-aware GRPO algorithm masks post-failure tokens while preserving pre-failure reasoning via one-sided advantage clamping, achieving 10+ point average gains across 7 benchmarks.

## Key Contributions

- Data curation pipeline for agentic RL: Wikipedia path sampling + fuzzy entity rewriting + visual grounding reduces retrieval shortcuts and one-step collapse
- Diverse 7-tool environment: text/image search, OCR, cropping, sharpening, super-resolution, perspective correction
- Multi-turn fatal-aware GRPO: masks tokens after cascading tool failures, clamps advantages one-sided to preserve pre-failure reasoning signal
- 10+ point average improvement across 7 benchmarks; matches proprietary commercial models on several tasks

## Relevance

Addresses an under-researched angle in the digest: how to construct the training data and environment for agentic VLM RL, not just the algorithm. Directly relevant to the tool use and VLM agent threads running through the entire digest; complements VISTA-R1 (tool-integrated VLM reasoning) with a concrete open-source data recipe.

## My Thoughts

<!-- Add your own notes here -->
