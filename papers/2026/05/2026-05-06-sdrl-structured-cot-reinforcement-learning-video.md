---
title: "Reinforcing Structured Chain-of-Thought for Video Understanding"
authors: ["Peiyao Wang", "Haotian Xu", "Noranart Vesdapunt", "Rui Hou", "Jingyi Zhang", "Haibin Ling", "Oleksandr Obiednikov", "Ning Zhou", "Kah Kuen Fu"]
date: 2026-03-26
arxiv_id: "2603.25942v1"
url: "https://arxiv.org/abs/2603.25942v1"
score: 0.84
topics: [GRPO, VLM, vision-language, multimodal, RL training]
status: unread
---

# Reinforcing Structured Chain-of-Thought for Video Understanding

## Summary

SDRL (Summary-Driven Reinforcement Learning) is a single-stage GRPO-based framework for video-understanding VLMs that eliminates SFT by using a Structured CoT format (Summarize→Think→Answer). It introduces two self-supervised mechanisms integrated into the GRPO objective: CVK (Consistency of Vision Knowledge), which enforces factual grounding by minimising KL divergence across generated summaries, and DVR (Dynamic Variety of Reasoning), which dynamically modulates thinking diversity based on group accuracy to balance alignment and exploration. The method achieves state-of-the-art on seven VideoQA benchmarks.

## Key Contributions

- Single-stage RL training for video VLMs: eliminates costly SFT and CoT annotation requirement
- Structured CoT format (Summarize→Think→Answer) provides scaffold without fixed reasoning paths
- CVK: self-supervised factual grounding via KL divergence minimization across generated video summaries
- DVR: dynamic exploration control based on group accuracy; prevents both mode collapse and random exploration

## Relevance

The CVK+DVR mechanisms are a direct application of the exploration/entropy-balance thread (PolicySplit, DEEP-GRPO, HeRL) to the video domain — but implemented as reward components inside GRPO rather than as policy modifications. The SFT-free single-stage approach also mirrors the RLAIF direction (Oracle-RLAIF) by removing expensive supervised data requirements.

## My Thoughts

<!-- Add your own notes here -->
