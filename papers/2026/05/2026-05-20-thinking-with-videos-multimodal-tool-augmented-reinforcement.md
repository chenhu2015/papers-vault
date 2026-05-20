---
title: "Thinking With Videos: Multimodal Tool-Augmented Reinforcement Learning for Long Video Reasoning"
authors: ["Haoji Zhang", "Xin Gu", "Jiawen Li", "Chixiang Ma", "Sule Bai", "Chubin Zhang", "Bowen Zhang", "Zhichao Zhou", "Dongliang He", "Yansong Tang"]
date: 2026-05-20
arxiv_id: "2508.04416v2"
url: "http://arxiv.org/abs/2508.04416v2"
score: 0.88
topics: [agentic RL, tool use, VLM, multimodal, GRPO]
status: unread
---

# Thinking With Videos: Multimodal Tool-Augmented Reinforcement Learning for Long Video Reasoning

## Summary

VITAL introduces an agentic video reasoning framework where the model uses visual tools to dynamically sample new frames during inference, generating multimodal chain-of-thought reasoning. Training combines SFT on a 72k CoT dataset followed by RL using Difficulty-aware GRPO (DGRPO), which weights samples by estimated difficulty to mitigate multi-task imbalance. The resulting model outperforms existing methods on 11 video understanding benchmarks, particularly excelling at long-video temporal grounding and question-answering tasks.

## Key Contributions

- Agentic visual toolbox: model can request new video frames on demand during reasoning, enabling dense cross-modal CoT
- MTVR-CoT-72k and MTVR-RL-110k: two new multi-task video reasoning datasets for SFT and RL stages respectively
- DGRPO (Difficulty-aware GRPO): reweights training samples by difficulty to prevent easy-task dominance in multi-task RL
- State-of-the-art on 11 video benchmarks for both video QA and temporal grounding, especially in long-video scenarios

## Relevance

This paper directly advances the agentic RL + tool use thread that has been a core focus of recent digests (ActFocus, AEM, CM2), now applied to the video VLM domain that the May 19 search identified as a high-value but underexplored cluster. DGRPO is a new GRPO variant addressing multi-task difficulty imbalance—a distinct contribution from step-level credit papers in recent days.

## My Thoughts

<!-- Add your own notes here -->
