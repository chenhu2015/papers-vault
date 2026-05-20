---
title: "Video-R2: Reinforcing Consistent and Grounded Reasoning in Multimodal Language Models"
authors: ["Muhammad Maaz", "Hanoona Rasheed", "Fahad Shahbaz Khan", "Salman Khan"]
date: 2026-05-20
arxiv_id: "2511.23478v2"
url: "http://arxiv.org/abs/2511.23478v2"
score: 0.87
topics: [VLM, multimodal, GRPO, reward model, vision-language]
status: unread
---

# Video-R2: Reinforcing Consistent and Grounded Reasoning in Multimodal Language Models

## Summary

Video-R2 diagnoses two failure modes in video reasoning models—Think-Answer Consistency (TAC) and Video Attention Score (VAS)—showing that current models heavily rely on linguistic priors rather than visual content across 11 benchmarks. The approach uses timestamp-aware SFT followed by GRPO with a novel Temporal Alignment Reward (TAR) that enforces temporally aligned and causally coherent video reasoning. Video-R2 achieves consistently higher TAC, VAS, and accuracy, demonstrating that explicit temporal grounding rewards improve trustworthy video understanding.

## Key Contributions

- TAC and VAS: two diagnostic metrics exposing reasoning-answer inconsistency and over-reliance on language priors in current video MLLMs
- Temporal Alignment Reward (TAR): a new reward signal for GRPO that penalizes temporally misaligned and causally incoherent video reasoning
- Two-stage post-training: timestamp-aware SFT → GRPO-TAR, improving both consistency metrics and downstream accuracy
- Evaluated across 11 diverse video reasoning benchmarks with open-source code

## Relevance

Connects directly to the VLM + GRPO thread and extends May 19's MoCA (modality-aware credit assignment) insight into the video domain: just as MoCA routes reward to perception vs reasoning, Video-R2's TAR routes reward to temporally grounded vs linguistically confabulated video reasoning. The TAC/VAS diagnostic framework could also inform future reward model design.

## My Thoughts

<!-- Add your own notes here -->
