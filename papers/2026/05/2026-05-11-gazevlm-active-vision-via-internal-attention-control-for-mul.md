---
title: "GazeVLM: Active Vision via Internal Attention Control for Multimodal Reasoning"
authors: ["Brown Ebouky", "Gabriele Carrino", "Niccolo Avogaro", "Christoph Studer", "Andrea Bartezzaghi", "Mattia Rigotti"]
date: 2026-05-08
arxiv_id: "2605.07817"
url: "http://arxiv.org/abs/2605.07817v1"
score: 0.82
topics: [GRPO, VLM, multimodal models, vision-language, reward model]
status: unread
---

# GazeVLM: Active Vision via Internal Attention Control for Multimodal Reasoning

## Summary

GazeVLM introduces learnable gaze tokens (<LOOK>) that give a VLM metacognitive control over its own causal attention mask, implementing top-down foveal fixation on task-relevant image regions while preserving global context. Trained with GRPO rewarding valid grounding, the 4B-parameter model surpasses state-of-the-art VLMs by ~4% on high-resolution benchmarks (HRBench-4k/8k) without external cropping tools or additional visual tokens. This directly addresses the passive visual processing bottleneck of current VLMs.

## Key Contributions

- Gaze tokens (<LOOK>) for internalizing metacognitive attention control into the VLM reasoning loop
- Continuous suppression bias on causal attention mask to simulate foveal fixation
- GRPO training with valid-grounding reward — no external image processing pipeline required
- ~4% improvement over SoTA VLMs and >5% over agentic multimodal pipelines on HRBench-4k/8k

## Relevance

This combines GRPO fine-tuning with a novel VLM architecture — a natural extension of prior VLM RL work (tool-integrated VLM reasoning, GUI agents) by internalizing the "tool use" directly into the attention mechanism. The focus on high-resolution visual reasoning also complements the multimodal interest profile.

## My Thoughts

<!-- Add your own notes here -->
