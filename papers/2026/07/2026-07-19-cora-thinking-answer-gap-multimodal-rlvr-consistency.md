---
title: "CORA: Analyzing and bridging thinking-answer gap in Multimodal RLVR via Consistency-Oriented Reasoning Alignment"
authors: ["Jiayue Cao", "Zhicong Lu", "Xuehan Sun", "Wei Jia", "Hongling Zheng", "Changyuan Tian", "Zichuan Lin", "Wenqian Lv", "Nayu Liu"]
date: 2026-06-12
arxiv_id: "2606.14691"
url: "https://arxiv.org/abs/2606.14691"
score: 0.81
topics: [multimodal models, vision language models, VLM, GRPO, RL training, reward model]
status: unread
---

# CORA: Analyzing and bridging thinking-answer gap in Multimodal RLVR via Consistency-Oriented Reasoning Alignment

## Summary

CORA identifies and analyzes thinking-answer inconsistency in multimodal RLVR — where the reasoning trace and the final answer are semantically inconsistent — showing the problem persists throughout GRPO training and remains at inference time via analysis of rollout trajectories. The proposed fix is a plug-and-play consistency reward model that introduces thinking-answer semantic consistency as an auxiliary reward signal, combined with Hybrid Reward Advantage Splitting (HRAS) to coordinate task and consistency optimization without interference. Experiments across multiple LVLMs and benchmarks show improved task performance alongside more faithful reasoning traces.

## Key Contributions

- Thinking-answer inconsistency: systematic empirical analysis showing this failure mode emerges and persists during GRPO training on multimodal data, not just at inference
- Consistency reward model: lightweight model assessing semantic alignment between CoT trace and final answer; plug-and-play, no retraining of base model required
- HRAS (Hybrid Reward Advantage Splitting): decomposes advantage computation to coordinate task reward and consistency reward without one dominating gradient updates
- Demonstrated on multiple LVLMs showing consistent improvement on reasoning benchmarks with more faithful traces

## Relevance

Addresses the VLM-specific gap in the vault's reward model thread. The thinking-answer inconsistency is distinct from the hallucination problem addressed by prior VLM RL papers (ViCrit); it targets the structural coherence of the CoT trace itself. HRAS is conceptually related to EGRSD's entropy gate (both modulate which signal dominates per-token or per-component update), but operates at the reward level rather than the token level.

## My Thoughts

<!-- Add your own notes here -->
