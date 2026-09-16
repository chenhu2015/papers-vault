---
title: "Advancing Multimodal Reasoning: From Optimized Cold Start to Staged Reinforcement Learning"
authors: ["Shuang Chen", "Yue Guo", "Zhaochen Su", "Yafu Li", "Yulun Wu", "Jiacheng Chen", "Jiayu Chen", "Weijie Wang", "Xiaoye Qu", "Yu Cheng"]
date: 2025-06-04
arxiv_id: "2506.04207v2"
url: "http://arxiv.org/abs/2506.04207v2"
score: 0.73
topics: [multimodal models, VLM, GRPO, RL training]
status: unread
---

# Advancing Multimodal Reasoning: From Optimized Cold Start to Staged Reinforcement Learning

## Summary

ReVisual-R1 identifies three underappreciated phenomena in multimodal GRPO training: (1) text-only cold-start initialization outperforms multimodal cold-start, (2) standard GRPO applied to multimodal RL causes gradient stagnation degrading stability and performance, and (3) appending text-only RL after multimodal RL further improves multimodal reasoning by balancing perceptual grounding and cognitive reasoning. The staged pipeline achieves SOTA among open-source 7B MLLMs on MathVerse, MathVision, WeMath, LogicVista, DynaMath, AIME2024, and AIME2025.

## Key Contributions

- Identifies GRPO gradient stagnation as a concrete failure mode specific to multimodal RL (not present in text-only RL)
- Text-only cold-start initialization consistently outperforms multimodal cold-start for MLLMs
- Staged training recipe: text cold-start → multimodal GRPO → text-only GRPO improves on multimodal-only pipelines
- SOTA on 7 challenging multimodal reasoning benchmarks at 7B scale

## Relevance

Directly closes a facet of the SFT-free VLM RL gap: not SFT-free, but characterizes the gradient stagnation failure mode that makes naive multimodal GRPO unstable. The finding that text-only cold-start beats multimodal cold-start is the most actionable result — it suggests that the SFT-free gap may be solvable by careful cold-start design rather than by removing SFT entirely.

## My Thoughts

<!-- Add your own notes here -->
