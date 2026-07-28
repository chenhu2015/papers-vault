---
title: "Offline-Online Curriculum RL for Multimodal Reasoning"
authors: ["Wendi Deng", "Hang Du", "Guoshun Nan", "Haokun Tian", "Jiaqi Yu", "Xinlei Cao", "Jaile Li", "Jingfeng Chen", "Ling Deng", "Ting Li", "Hao Yang", "Jun Liu", "Xudong Jiang", "Sicong Leng"]
date: 2026-07-28
arxiv_id: "2607.23700"
url: "https://arxiv.org/abs/2607.23700"
score: 0.82
topics: [multimodal models, vision language models, VLM, agentic RL, GRPO, RL training]
status: unread
---

# Offline-Online Curriculum RL for Multimodal Reasoning

## Summary

Proposes O²-CritiCuRL, a curriculum RL framework for multimodal reasoning that identifies critical reasoning steps through offline multi-rollout analysis of step-annotated trajectories, then uses a progressive online RL stage where truncated chains guide the model to infer and refine missing decisive steps. The offline-online iteration filters redundant steps, sharpens gradient focus on causally important reasoning transitions, and achieves state-of-the-art performance on multimodal benchmarks with improved training and inference efficiency.

## Key Contributions

- Offline stage: multi-rollout analysis over step-annotated trajectories estimates step-level importance, distilling critical steps and filtering redundant ones
- Online stage: progressive step-level RL with truncated chains guides the model to infer missing critical steps and refine its reasoning
- Iterative offline-online paradigm that avoids static supervision limitations and continuously sharpens curriculum quality
- SOTA on multimodal reasoning benchmarks with superior training efficiency versus static step supervision baselines

## Relevance

Connects to two active threads: (1) the credit assignment thread (STAPO Jul 26 uses normalized entropy to identify neglect-prone steps; O²-CritiCuRL uses multi-rollout offline analysis to identify critical steps — both target step-level gradient allocation but via different signals); (2) the VLM RL curriculum thread (PATS Jul 25 adapts training context dynamically; O²-CritiCuRL uses offline step identification to drive online curriculum, providing a principled two-stage alternative).

## My Thoughts

<!-- Add your own notes here -->
