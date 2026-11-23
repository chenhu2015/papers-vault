---
title: "MoD-DPO: Towards Mitigating Cross-modal Hallucinations in Omni LLMs using Modality Decoupled Preference Optimization"
authors: ["Ashutosh Chaubey", "Jiacheng Pang", "Mohammad Soleymani"]
date: 2026-03-03
arxiv_id: "2603.03192"
url: "https://arxiv.org/abs/2603.03192"
score: 0.73
topics: [multimodal models, vision language models, RLHF]
status: unread
---

# MoD-DPO: Towards Mitigating Cross-modal Hallucinations in Omni LLMs using Modality Decoupled Preference Optimization

## Summary

MoD-DPO extends DPO to Omni-modal LLMs (audio-visual-text) by decoupling modality contributions: modality-aware regularization enforces invariance to irrelevant-modality perturbations and sensitivity to relevant ones, while a language-prior debiasing penalty suppresses hallucination-prone text-only responses. Evaluated on audiovisual hallucination benchmarks, MoD-DPO consistently outperforms DPO and other preference optimization baselines for multimodal grounding.

## Key Contributions

- Modality-aware regularization terms that penalize sensitivity to irrelevant modality corruptions and reward sensitivity to relevant modality perturbations
- Language-prior debiasing penalty to reduce over-reliance on text-only predictions that bypass visual/audio evidence
- Demonstration that standard DPO fails on Omni-modal LLMs due to spurious cross-modal correlations and dominant language priors
- Outperforms prior preference optimization baselines on multiple audiovisual hallucination benchmarks under similar training budgets

## Relevance

Extends the multimodal RL training thread (Gaze-RL, ThinkWise, Omni-AutoThink) to the preference optimization setting: where most prior multimodal alignment work applies DPO naively, MoD-DPO shows that modality decoupling is necessary for Omni-modal LLMs. Distinct angle from RLVR/GRPO-based training — DPO-side alignment for audio-visual-text models.

## My Thoughts

<!-- Add your own notes here -->
