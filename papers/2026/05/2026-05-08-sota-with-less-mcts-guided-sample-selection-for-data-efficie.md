---
title: "SoTA with Less: MCTS-Guided Sample Selection for Data-Efficient Visual Reasoning Self-Improvement"
authors: ["Xiyao Wang", "Zhengyuan Yang", "Chao Feng", "Hongjin Lu", "Linjie Li", "Chung-Ching Lin", "Kevin Lin", "Furong Huang", "Lijuan Wang"]
date: 2025-04-10
arxiv_id: "2504.07934v3"
url: "https://arxiv.org/abs/2504.07934v3"
score: 0.83
topics: [reinforcement learning, RL training, multimodal models, vision language models, VLM]
status: unread
---

# SoTA with Less: MCTS-Guided Sample Selection for Data-Efficient Visual Reasoning Self-Improvement

## Summary

ThinkLite-VL repurposes MCTS to measure sample difficulty for reinforcement fine-tuning (RFT) of visual reasoning VLMs, selecting just 11k challenging examples from 70k by counting how many MCTS iterations a model needs to solve each instance. The resulting 7B model surpasses GPT-4o, O1, and Qwen2.5-VL-72B on MathVista (75.1), achieving SoTA with an order of magnitude fewer training samples and no knowledge distillation. MCTS-guided difficulty filtering proves a scalable, distillation-free path to data-efficient RL self-improvement in multimodal reasoning.

## Key Contributions

- MCTS repurposed as a difficulty oracle: iteration count to solve = sample difficulty signal for RFT selection
- 11k-sample RFT (from 70k) on Qwen2.5-VL-7B beats GPT-4o, O1, and 72B models on MathVista (75.1)
- ThinkLite-VL-72B advances open-source SoTA with 79.7 on MathVista, +4.42 avg over prior SOTA
- Distillation-free: no teacher model needed, self-improvement via RL on curated challenging samples

## Relevance

Directly extends the data curation for RL thread (OpenSearch-VL, DEPO from May 7) with a principled MCTS-based difficulty measure for VLM RFT, showing that sample quality beats quantity even for visual reasoning. The group-relative RFT framing connects naturally to the GRPO/RLVR papers throughout the digest.

## My Thoughts

<!-- Add your own notes here -->
