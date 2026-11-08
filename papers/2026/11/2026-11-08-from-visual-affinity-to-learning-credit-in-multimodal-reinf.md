---
title: "From Visual Affinity to Learning Credit in Multimodal Reinforcement Learning"
authors: ["Yuhang Han", "Dingning Liu", "Yujie Chen", "Yaojie Zhang", "Jingwei Song", "Zequn Yang", "Xuanming Shang", "Li Ding", "Zhijiang Guo", "Linfeng Zhang"]
date: 2026-10-23
arxiv_id: "2610.32324v1"
url: "https://arxiv.org/abs/2610.32324"
score: 0.88
topics: [multimodal models, vision language models, VLM, GRPO, agentic RL]
status: unread
---

# From Visual Affinity to Learning Credit in Multimodal Reinforcement Learning

## Summary

OVC (Outcome-Conditioned Visual Credit) decouples visual-association measurement from token-level credit assignment in multimodal RLVR, constructing a context-relative visual coordinate by contrasting each predictive state's affinity to image vs. prompt-context representations. The core insight is that visual affinity alone is insufficient — a token aligned with a correct observation still receives a negative advantage update when subsequent reasoning fails, so credit must be calibrated against observed outcome differences (positive vs. negative responses) rather than affinity alone. Instantiated as GSPO-token, OVC improves six-benchmark mean accuracy by 1.86–2.39pp over GSPO across three models with no extra rollouts or auxiliary models.

## Key Contributions

- Relative Visual Encoding: constructs a context-relative coordinate by contrasting predictive state affinity to image vs. prompt-context representations, disentangling visual from textual signal
- Outcome-conditioned Evidence Calibration: combines the visual coordinate with uncertainty-scaled predictive features; calibrates contributions via mean contrasts between positive/negative responses, scaled by within-side variation
- Normalized Credit Allocation: conditions calibrated evidence on advantage sign to produce positive token weights with unit global mean, preserving advantage signs while modulating individual gradient contributions
- No auxiliary models or extra rollouts: OVC reuses existing GSPO rollouts; GSPO-token instantiation yields +1.86–2.39pp across six benchmarks and three models

## Relevance

Directly advances the VLM RL reward design thread: OVC is the first mechanism to explicitly condition visual token credit on outcome-discriminative evidence rather than affinity, complementing TACE (distributional normalization + budget-neutral credit, Nov 7) and distinguishing itself from attention-graph methods (AttnSR) by operating at the cross-response contrast level. Identified via the MLLM/calibration vocabulary pivot recommended after Nov 6's search strategy analysis.

## My Thoughts

<!-- Add your own notes here -->
