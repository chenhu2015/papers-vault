---
title: "What Do Verifiable Rewards Teach Video-Language Models About Time? A Controlled Multi-Model Study"
authors: ["Avyay Sadhu", "Patrick Cooper"]
date: 2026-10-14
arxiv_id: "2610.03792v1"
url: "http://arxiv.org/abs/2610.03792v1"
score: 0.75
topics: [multimodal models, vision language models, VLM, GRPO, RL training, RLHF]
status: unread
---

# What Do Verifiable Rewards Teach Video-Language Models About Time? A Controlled Multi-Model Study

## Summary

Fine-tunes four open video-language models (Qwen3-VL, Qwen2.5-VL, Gemma-3) with GRPO under three data recipes (verified synthetic, unverified real, mixture) and finds that verified-only training can severely degrade out-of-domain accuracy (up to -26.7 points) with no warning signal during training, while mixing in real video prevents degradation while preserving in-domain gains. A central finding is that no recipe induces temporal-order grounding — across 41 evaluations the ordered-vs-shuffled gap is consistently near zero despite explicit event-order rewards. The diagnosis is narrow synthetic-only data, not RLVR itself, and the paper advocates always reporting no-frame controls to disentangle visual from non-visual gains.

## Key Contributions

- Systematic 4-model × 3-recipe controlled study of RLVR for video-language understanding
- Verified-only training causes silent OOD degradation (-26.7 pts for Qwen3-VL-8B); mixture training is the fix
- No recipe induces temporal-order grounding despite event-order rewards: ordered-vs-shuffled gap ≈ 0 across 41 evals
- Methodological norm: always report no-frame controls and OOD evaluation for multimodal RLVR papers

## Relevance

Extends the multimodal RL thread by showing that even with explicit temporal rewards, GRPO does not induce structural visual grounding in video-LMs — a direct counterpart to "Same Reward, Different Skills" in the video domain. The silent OOD degradation finding is a practical warning for the VLM RL credit cluster: credit assignment improvements may mask underlying distributional brittleness.

## My Thoughts

<!-- Add your own notes here -->
