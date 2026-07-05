---
title: "Reasoning as Intersection: Consensus-Frame Alignment for Visual Focus in Video-MLLMs"
authors: ["Chengwen Liu", "Zhe Huang", "Jisheng Dang", "Hong Peng", "Qi Tian", "Tat-Seng Chua"]
date: 2026-07-05
arxiv_id: "2606.18441"
url: "https://arxiv.org/abs/2606.18441"
score: 0.82
topics: [VLM, multimodal models, RL training, GRPO]
status: unread
---

# Reasoning as Intersection: Consensus-Frame Alignment for Visual Focus in Video-MLLMs

## Summary

CF-GRPO introduces a temporal-annotation-free process-level reward for training video MLLMs via GRPO, constructing a consensus frame prior from intrinsic video cues (temporal coverage, scene transitions, query relevance) and optimizing agreement with model-side frame-use scores via the Consensus Frame Reward (CFR). CFR provides a high-contrast dense signal guiding which visual evidence should support the answer without requiring human temporal annotations. VideoCFR achieves competitive performance across complex video reasoning benchmarks over RL baselines.

## Key Contributions

- Consensus Frame Prior: built from temporal coverage, scene-transition cues, and query-conditioned visual relevance — no human temporal annotations required
- Consensus Frame Reward (CFR): optimizes agreement between the prior and model-side frame-use scores extracted from visual and response representations
- Salience-aware sparse aggregation and distribution sharpening for high-contrast reward signal
- Shows that process-level rewards for video MLLMs can be derived entirely from intrinsic video structure

## Relevance

CF-GRPO extends the process reward thread — established for text RL (PASS, Jul 1), RAG agents (ReasonRAG, Jul 4), and GUI agents (VisCritic, Jul 4) — into the video temporal domain, applying annotation-free GRPO process supervision to video-MLLMs. The consensus frame prior is structurally analogous to VisCritic's Siamese pre/post-action screenshot comparison: both derive a visual process signal without text-only verification, and both operate on domain-appropriate visual witnesses (GUI state changes vs. video frame relevance).

## My Thoughts

<!-- Add your own notes here -->
