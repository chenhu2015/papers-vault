---
title: "Exploring More, Reasoning Better: Stepwise Risk-Sensitive GRPO for Diffusion Language Models"
authors: ["Yue Yu", "Bowen Zuo", "David Crandall", "Yinglun Zhu", "Dongruo Zhou"]
date: 2026-10-19
arxiv_id: "2610.00661v2"
url: "http://arxiv.org/abs/2610.00661v2"
score: 0.82
topics: [GRPO, RL training, reward model]
status: unread
---

# Exploring More, Reasoning Better: Stepwise Risk-Sensitive GRPO for Diffusion Language Models

## Summary

StepRS-GRPO varies the risk coefficient of the group-advantage transformation across denoising states in dLLMs, showing for binary rewards that this equals a prompt-and-state-dependent rescaling of centered outcome advantages. Across multiple dLLM backbones and math benchmarks, StepRS-GRPO improves both pass@1 accuracy and pass@k coverage over centered GRPO while increasing answer diversity, with capability-based calibration and ablations establishing the contribution of state allocation and schedule direction.

## Key Contributions

- Risk coefficient schedule over denoising states: different states get different advantage scaling
- Theoretical equivalence to state-dependent advantage rescaling for binary rewards
- Capability-based calibration to choose coefficient scale + schedule selection ablations
- Improves pass@1 and pass@k coverage, with increased answer diversity as a diagnostic

## Relevance

Sixth paper in the diffusion LM RL thread. Complements StepRS-GRPO's state-dependent perspective to DiSPO's branching approach: both are concerned with how to treat different denoising states differently, but StepRS-GRPO does so through advantage scaling rather than credit branching. Pairs with StepRS-GRPO on the same axis as PACT (step-credit) and GDPO (objective) but at the advantage-weighting level.

## My Thoughts

<!-- Add your own notes here -->
