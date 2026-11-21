---
title: "Omni-AutoThink: Adaptive Multimodal Reasoning via Reinforcement Learning"
authors: ["Dongchao Yang", "Songxiang Liu", "Disong Wang", "Yuanyuan Wang", "Guanglu Wan", "Helen Meng"]
date: 2025-12-03
arxiv_id: "2512.03783"
url: "https://arxiv.org/abs/2512.03783"
score: 0.80
topics: [agentic RL, multimodal models, GRPO, reinforcement learning, VLM]
status: unread
---

# Omni-AutoThink: Adaptive Multimodal Reasoning via Reinforcement Learning

## Summary

Omni-AutoThink proposes adaptive reasoning for Omni (audio-visual-text) models in two stages: Adaptive SFT seeds reasoning capability on large-scale reasoning-augmented data, then Adaptive GRPO optimizes reasoning depth based on task complexity and reward feedback. It introduces a comprehensive adaptive reasoning benchmark spanning text-only, text-audio, text-visual, and text-audio-visual modalities, significantly improving over rigid always-think/never-think baselines.

## Key Contributions

- Two-stage adaptive training: Adaptive SFT for initialization, then Adaptive GRPO for dynamic depth adjustment
- Adaptive GRPO extends GRPO with complexity-conditioned reasoning allocation
- Covers all four modality combinations (text, text-audio, text-visual, text-audio-visual) in one framework
- Introduces a new multi-modal adaptive reasoning benchmark for both training and evaluation

## Relevance

Extends the ThinkWise/DR-BOLT/TON adaptive reasoning cluster to Omni models, adding the audio modality which has not appeared in prior digests. The Adaptive GRPO stage is architecturally similar to TON's unconstrained GRPO but adds a complexity-conditioning signal, making it complementary — TON learns when to skip reasoning, Omni-AutoThink learns how deep to reason.

## My Thoughts

<!-- Add your own notes here -->
