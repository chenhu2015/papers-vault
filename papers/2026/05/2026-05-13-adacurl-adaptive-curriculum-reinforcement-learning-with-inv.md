---
title: "AdaCuRL: Adaptive Curriculum Reinforcement Learning with Invalid Sample Mitigation and Historical Revisiting"
authors: ["Renda Li", "Hailang Huang", "Fei Wei", "Feng Xiong", "Yong Wang", "Xiangxiang Chu"]
date: 2025-11-12
arxiv_id: "2511.09478v1"
url: "http://arxiv.org/abs/2511.09478v1"
score: 0.83
topics: [RL training, GRPO, agentic RL, multimodal models, reinforcement learning]
status: unread
---

# AdaCuRL: Adaptive Curriculum Reinforcement Learning with Invalid Sample Mitigation and Historical Revisiting

## Summary

AdaCuRL addresses two distinct failure modes in RLVR training: gradient starvation (easy samples producing zero gradients) and policy degradation (unstable updates from hard samples), both arising from training on mixed-difficulty batches. It introduces coarse-to-fine difficulty estimation with adaptive curriculum scheduling to align data difficulty with model capability, a historical revisitation mechanism to prevent catastrophic forgetting, and adaptive reference + sparse KL to stabilize policy updates. Experiments across diverse reasoning benchmarks show consistent gains over GRPO, DAPO, and GSPO baselines on both LLMs and MLLMs.

## Key Contributions

- Formalizes two RLVR failure modes: gradient starvation (all-correct/all-wrong batches) and policy degradation (too-hard batches causing collapse)
- Coarse-to-fine difficulty estimation: assigns difficulty scores without manual annotation
- Adaptive curriculum scheduler that dynamically aligns training difficulty with current model competence
- Historical revisitation to prevent catastrophic forgetting of previously mastered difficulty levels
- Adaptive reference policy + sparse KL regularization to prevent policy collapse during hard-sample training

## Relevance

Directly addresses core limitations in GRPO/RLVR training pipelines — the failure modes of gradient starvation and policy degradation are practical engineering problems in the exact training paradigm (GRPO-based RLVR) that drives the RL training and agentic RL interests. Works on both LLMs and MLLMs, spanning both multimodal and language-only portions of the interest profile.

## My Thoughts

<!-- Add your own notes here -->
