---
title: "Think, Compress, Answer: Reinforcement Learning for Multimodal Grounding via Reasoning Compression"
authors: ["Jinbae Seo", "Hyeongjun Kwon", "Jiyoung Lee", "Hyunsung Jang", "Namkoo Ha", "Jungin Park", "Kwanghoon Sohn"]
date: 2026-10-19
arxiv_id: "2610.25640"
url: "https://arxiv.org/abs/2610.25640"
score: 0.80
topics: [VLM, multimodal models, vision-language, GRPO, reward model, agentic RL]
status: unread
---

# Think, Compress, Answer: Reinforcement Learning for Multimodal Grounding via Reasoning Compression

## Summary

TCA (Think-Compress-Answer) decomposes MLLM grounding into free-form reasoning, target-aware context compression guided by the information bottleneck principle, and answer generation from the compressed context. Optimized via multi-stage GRPO with progressive rewards that establish the structured output protocol, minimize reasoning-specific information while preserving target-relevant content, and directly improve localization accuracy. Zero-shot performance gains across six multimodal grounding benchmarks demonstrate that reasoning compression retains the benefits of extended reasoning while distilling it into the minimal context required for grounding.

## Key Contributions

- Three-phase decomposition: Think (free-form reasoning) → Compress (IB-guided target-aware compression) → Answer (from compressed context)
- Multi-stage GRPO with progressive rewards: stage 1 establishes structured protocol, stage 2 minimizes reasoning-specific information while preserving target content, stage 3 improves localization accuracy
- Information bottleneck as the theoretical principle for why long reasoning can dilute grounded perceptual evidence
- Zero-shot gains across six multimodal grounding benchmarks without task-specific adaptation

## Relevance

This paper is the second new entry for the VLM RL reward design thread today alongside Aerial-R1, and it complements TACE (Nov 7, budget-neutral credit + distributional normalization) with an orthogonal approach: rather than fixing how credit is allocated across tokens, TCA fixes what information the reasoning trace carries into the answer generation stage. OVC (Nov 8) separated visual affinity from credit assignment; TCA separates reasoning richness from grounding-relevant content — a structurally parallel insight applied at the generation stage.

## My Thoughts

<!-- Add your own notes here -->
