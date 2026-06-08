---
title: "RL Excursions during Pre-Training: Re-examining Policy Optimization for LLM training"
authors: ["Rachit Bansal", "Clara Mohri", "Tian Qin", "David Alvarez-Melis", "Sham Kakade"]
date: 2026-06-02
arxiv_id: "2606.04272v1"
url: "http://arxiv.org/abs/2606.04272v1"
score: 0.77
topics: [RL training, RLHF, reinforcement learning, GRPO, PPO]
status: unread
---

# RL Excursions during Pre-Training: Re-examining Policy Optimization for LLM training

## Summary

This paper challenges the assumption that RL must follow SFT post-training by applying RL directly to intermediate pre-training checkpoints. They find RL is effective very early and often matches the full SFT→RL pipeline; targeted pre-training data composition matters more than model scale for RL effectiveness. Parallel averaging of RL and SFT objectives outperforms all other training configurations while preserving general capabilities that SFT degrades.

## Key Contributions

- Systematic comparison of RL applied at different stages: base, intermediate pre-training, post-SFT
- Finding that RL is effective surprisingly early and data composition is more important than scale
- Sharpening effect (distribution narrowing) only occurs when RL follows SFT, not when RL is applied to base
- Parallel averaging of RL + SFT objectives achieves best performance across all metrics while preserving general capabilities

## Relevance

Opens a new angle on the RL training pipeline not covered in recent digests — when and how RL interacts with pre-training vs. SFT stages. The parallel averaging finding is particularly relevant to practical LLM training setups and connects with the training stability thread (EP-GRPO/M-GRPO from June 2).

## My Thoughts

<!-- Add your own notes here -->
