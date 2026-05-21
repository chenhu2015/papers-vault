---
title: "AutoRubric: Rubric-Based Generative Rewards for Faithful Multimodal Reasoning"
authors: ["Mengzhao Jia", "Zhihan Zhang", "Ignacio Cases", "Zheyuan Liu", "Meng Jiang", "Peng Qi"]
date: 2025-10-16
arxiv_id: "2510.14738v2"
url: "http://arxiv.org/abs/2510.14738v2"
score: 0.78
topics: [RLAIF, reward model, multimodal, VLM, vision-language, reinforcement learning]
status: unread
---

# AutoRubric: Rubric-Based Generative Rewards for Faithful Multimodal Reasoning

## Summary

AutoRubric integrates RLVR with process-level supervision through automatically constructed rubric-based generative rewards, using a scalable self-aggregation method that distills consistent reasoning checkpoints from successful trajectories without human annotation or stronger teacher models. Joint rubric-based and outcome rewards address the spurious reasoning problem in RLVR—where only final-answer correctness is rewarded—achieving state-of-the-art on six multimodal reasoning benchmarks with substantially improved faithfulness.

## Key Contributions

- Self-aggregation method: distills consistent reasoning checkpoints from successful rollouts to build problem-specific rubrics automatically
- Rubric-based generative reward provides process-level supervision without human annotation or teacher models
- Joint optimization of rubric-based and outcome rewards reduces spurious/shortcut reasoning in RLVR
- State-of-the-art on six multimodal reasoning benchmarks with improved faithfulness metrics

## Relevance

Bridges the VLM/multimodal thread with the process reward and faithfulness threads. The self-aggregation approach for rubric construction is a zero-cost alternative to external PRMs, complementing V-tableR1 (May 18) and SRaR (May 19) which also pursued process-level reward supervision.

## My Thoughts

<!-- Add your own notes here -->
