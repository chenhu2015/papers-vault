---
title: "SenseNova-MARS: Empowering Multimodal Agentic Reasoning and Search via Reinforcement Learning"
authors: ["Yong Xien Chng", "Tao Hu", "Wenwen Tong", "Xueheng Li", "Jiandong Chen", "Haojia Yu", "Jiefan Lu", "Hewei Guo", "Hanming Deng", "Chengjun Xie", "Gao Huang", "Dahua Lin", "Lewei Lu"]
date: 2026-06-06
arxiv_id: "2512.24330v2"
url: "http://arxiv.org/abs/2512.24330v2"
score: 0.84
topics: [multimodal models, vision-language, VLM, agentic, tool use, GRPO, agentic RL]
status: unread
---

# SenseNova-MARS: Empowering Multimodal Agentic Reasoning and Search via Reinforcement Learning

## Summary

SenseNova-MARS trains VLMs to interleave dynamic tool invocation (image search, text search, image crop) with visual reasoning via reinforcement learning, introducing BN-GSPO (Batch-Normalised Group Sequence Policy Optimisation) to stabilise training. On search-oriented benchmarks, SenseNova-MARS-32B achieves 74.3 on MMSearch and 54.4 on HR-MMSearch, surpassing proprietary models including Gemini-3-Pro and GPT-5.2. The work demonstrates that multimodal agentic tool-use capability is achievable through RL without sacrificing visual understanding quality.

## Key Contributions

- Introduces interleaved visual reasoning + tool invocation training via RL (image search, text search, crop tools)
- BN-GSPO: Batch-Normalised Group Sequence Policy Optimisation improves training stability for long multimodal agentic trajectories
- Introduces HR-MMSearch: first search-oriented benchmark with high-resolution knowledge-intensive images
- SenseNova-MARS-32B sets SOTA on open-source search and fine-grained image understanding benchmarks

## Relevance

This fills the VLM/computer-use RL gap that had been a carry-forward since May 31 (PRO-CUA). SenseNova-MARS goes further than prior GUI/computer-use RL by combining multimodal search with image manipulation tools, and the BN-GSPO algorithm is a GRPO variant worth tracking alongside EP-GRPO and M-GRPO from June 2.

## My Thoughts

<!-- Add your own notes here -->
