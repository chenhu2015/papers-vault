---
title: "ThinkWise: Learning When to Think in Large Multimodal Reasoning Models via Visual and Difficulty Perception"
authors: ["Wenkang Zhou", "Chen Yang", "Jiaheng Peng", "Xitong Li", "Hongzhi Yin", "Yunke Zhang", "Lu Yu", "Peng-Fei Zhang", "Xuhui Ren", "Shijie Zhang"]
date: 2026-11-02
arxiv_id: "2611.18685v1"
url: "http://arxiv.org/abs/2611.18685v1"
score: 0.78
topics: [VLM, vision-language models, multimodal models, reinforcement learning, GRPO]
status: unread
---

# ThinkWise: Learning When to Think in Large Multimodal Reasoning Models via Visual and Difficulty Perception

## Summary

ThinkWise proposes a perception-aware RLVR framework for VLMs that jointly models visual perception uncertainty and task difficulty to regulate reasoning depth, addressing Reasoning Allocation Misalignment (over-allocation of deep reasoning under uncertain visual grounding). The structured reward formulation combines an answer correctness reward, a perception-and-difficulty-conditioned length reward, and a perception reward for visual grounding, consistently improving accuracy-efficiency trade-offs across 3B and 7B models on multiple multimodal benchmarks.

## Key Contributions

- Identifies Reasoning Allocation Misalignment: VLMs waste deep reasoning tokens when visual perception is uncertain, hurting both efficiency and quality
- Instance-adaptive visual perception modeling: context-aware calibration of perception uncertainty at inference
- Three-part reward: correctness + perception-conditioned length (adaptive) + perception quality — structured decomposition specific to multimodal tasks
- Validated on 3B and 7B scales; holds across multiple benchmark distributions

## Relevance

First vault entry addressing the interaction between visual perception quality and reasoning depth in RLVR for VLMs. Complements Gaze-RL (intra-trajectory reward redistribution) with a different angle: pre-trajectory routing. Together they represent two orthogonal approaches to making multimodal RL more perceptually grounded.

## My Thoughts

<!-- Add your own notes here -->
