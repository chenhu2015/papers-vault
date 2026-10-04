---
title: "PF-RL: Progress Field Reinforcement Learning via Goal-Conditioned Value Geometry for Vision-Language-Action Models"
authors: ["Yunpeng Qing", "Yilun Kong", "Sixu Lin", "Ming Zhou", "Yiming Fei", "Shuang Luo", "Yixiao Chi", "Haoming Gu", "Jingyuan Liu", "Changxu Wei", "Zhi Hou", "Changqing Zou"]
date: 2026-10-04
arxiv_id: "2609.32634"
url: "https://arxiv.org/abs/2609.32634"
score: 0.73
topics: [VLM, multimodal models, vision-language, RL training, reward model]
status: unread
---

# PF-RL: Progress Field Reinforcement Learning via Goal-Conditioned Value Geometry for Vision-Language-Action Models

## Summary

PF-RL introduces a structured goal-conditioned progress representation (progress field) for Vision-Language-Action policies to provide dense transition-level credit in long-horizon manipulation, replacing the scalar progress estimates used by prior work. The progress field captures geometric structure in how intermediate observations relate to the task goal, enabling richer intermediate credit assignment without external annotations. Applied to VLA robotics, PF-RL consistently outperforms sparse-reward baselines and prior scalar-progress methods on long-horizon manipulation benchmarks.

## Key Contributions

- Progress field: structured goal-conditioned value geometry replacing scalar progress scalar for VLA models
- Transition-level dense credit without external annotations — goal geometry is derived from the pretrained VLA's own representations
- Addresses credit sparsity in long-horizon robotic manipulation — the domain analogue of the LLM agent sparse-reward problem
- Consistent improvement over scalar-progress baselines on manipulation benchmarks

## Relevance

PF-RL is the robotics-domain analogue of the no-gold-labels dense reward cluster (T2SPO, RFPO, TASPO), using goal-conditioned geometric structure rather than trajectory regression or frozen critics as the annotation-free credit signal. Its appearance in a VLA context suggests the step-credit design space is converging across language-agent and embodied-agent settings — the core problem (annotation-free dense credit for long-horizon sequential decisions) is identical, only the modality and action space differ.

## My Thoughts

<!-- Add your own notes here -->
