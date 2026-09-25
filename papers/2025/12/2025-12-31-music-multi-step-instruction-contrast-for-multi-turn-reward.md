---
title: "MUSIC: MUlti-Step Instruction Contrast for Multi-Turn Reward Models"
authors: ["Wenzhe Li", "Shujian Zhang", "Wenxuan Zhou", "John Lambert", "Chi Jin", "Andrew Hard", "Rajiv Mathews", "Lun Wang"]
date: 2025-12-31
arxiv_id: "2512.24693v1"
url: "https://arxiv.org/abs/2512.24693"
score: 0.70
topics: [RLHF, reward model, LLM agent]
status: unread
---

# MUSIC: MUlti-Step Instruction Contrast for Multi-Turn Reward Models

## Summary

MUSIC identifies that standard preference datasets contrasting only the final turn provide insufficient signal for multi-turn reward models, and proposes an unsupervised data augmentation strategy that synthesizes contrastive conversation pairs exhibiting differences across multiple turns. Applying MUSIC to the Skywork preference dataset yields a multi-turn RM that outperforms baselines on multi-turn conversation judgment without hurting single-turn RM benchmarks. This complements multi-turn GRPO training pipelines where per-step reward quality matters.

## Key Contributions

- Diagnoses a signal insufficiency in standard RLHF preference datasets for multi-turn settings: contrasting only the final turn cannot capture nuances of multi-turn interactions
- Proposes MUSIC: unsupervised data augmentation that synthesizes contrastive conversation pairs with differences spanning multiple turns, requiring no additional human annotation
- Trains a Gemma-2-9B-Instruct multi-turn RM using MUSIC-augmented Skywork preferences; outperforms baselines on multi-turn conversation quality alignment with advanced LLM judges
- Critically preserves single-turn RM benchmark performance, showing no regression from multi-turn specialization

## Relevance

Connects to the reward model thread from earlier digests (Omni-Thinker's LLM-as-Judge, Le Critique's privileged value functions). Multi-turn reward model quality is a direct upstream dependency for GRPO-based agentic RL training — if the reward model cannot distinguish multi-turn quality differences, step-level credit methods like GRAFT/SALT have limited signal to work with. MUSIC provides a cheap way to improve multi-turn RM quality without additional labeling.

## My Thoughts

<!-- Add your own notes here -->
