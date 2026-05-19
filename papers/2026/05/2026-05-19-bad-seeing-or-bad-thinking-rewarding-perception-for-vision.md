---
title: "Bad Seeing or Bad Thinking? Rewarding Perception for Vision-Language Reasoning"
authors: ["Haozhe Wang", "Qixin Xu", "Changpeng Wang", "Taofeng Xue", "Chong Peng", "Wenhu Chen", "Fangzhen Lin"]
date: 2026-05-13
arxiv_id: "2605.14054v1"
url: "http://arxiv.org/abs/2605.14054v1"
score: 0.83
topics: [VLM, vision-language, multimodal, reward model, RL training]
status: unread
---

# Bad Seeing or Bad Thinking? Rewarding Perception for Vision-Language Reasoning

## Summary

MoCA addresses the VLM 'seesaw effect' where improving perception degrades reasoning and vice versa by introducing Modality-Aware Credit Assignment that routes RL reward signals to the specific source of error — bad perception or bad logic. Perception Verification uses a 'blindfolded reasoning' proxy to reward perceptual fidelity independently of reasoning outcomes, while Structured Verbal Verification replaces high-variance LLM judging with structured algorithmic execution. MoCA enables simultaneous gains across perception and reasoning tasks from a single VLM.

## Key Contributions

- Identifies the seesaw effect: standard VLM RL conflates perception and reasoning errors, rewarding/penalizing the wrong modality
- Perception Verification (PV): a "blindfolded reasoning" proxy that evaluates perceptual fidelity by testing whether the model can reason correctly when given ground-truth visual information — isolating the perceptual credit signal
- Structured Verbal Verification replaces LLM-judge reward computation with deterministic structured execution, reducing reward variance at scale
- MoCA mechanism routes credit to the specific failure source, enabling a single VLM to simultaneously improve on both perception-heavy and reasoning-heavy tasks without trade-off

## Relevance

A novel angle on VLM RL that hasn't appeared in 18 days of digests: modality-specific credit assignment. Connects to the V-tableR1/structured visual RL thread (May 18) but addresses the fundamental reward attribution problem rather than specific task design. The blindfolded reasoning proxy is a clean methodological contribution.

## My Thoughts

<!-- Add your own notes here -->
