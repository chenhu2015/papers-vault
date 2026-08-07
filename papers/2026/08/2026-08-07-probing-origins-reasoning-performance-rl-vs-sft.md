---
title: "Probing the Origins of Reasoning Performance: Representational Quality for Mathematical Problem-Solving in RL vs. SFT Fine-Tuned Models"
authors: ["Antyabha Rahman", "Akshaj Gurugubelli", "Omar Ankit", "Kevin Zhu"]
date: 2026-07-28
arxiv_id: "2607.26119v1"
url: "https://arxiv.org/abs/2607.26119"
score: 0.79
topics: [reinforcement learning, RL training, LLM agent]
status: unread
---

# Probing the Origins of Reasoning Performance: Representational Quality for Mathematical Problem-Solving in RL vs. SFT Fine-Tuned Models

## Summary

This paper probes the mechanistic basis for RL models' superior math reasoning via layer-wise representation analysis. Linear probes show RL models develop more linearly separable, structured representations for predicting answer correctness, while mean ablation studies reveal a hierarchical architecture where deeper layers become progressively more critical — contrasting with SFT's uniform layer importance. Token-count variability analysis under repeated sampling suggests token allocation depends more on the overall training pipeline than on RL vs. SFT alone, pointing toward training-regime interactions as a key variable.

## Key Contributions

- Linear probes on layer-wise hidden states: RL models achieve higher accuracy in predicting answer correctness than SFT models, indicating more structured representations
- Mean ablation studies: RL models develop hierarchical architecture (deeper layers progressively more critical); SFT distributes importance uniformly across layers
- Token-count variability under repeated sampling: some RL models show higher variability (broader on-policy reasoning spread), others show strong consistency — suggests pipeline-dependent behavior rather than RL-inherent
- Frames token allocation variability as revealing "under-determined, potentially non-identifiable solution behavior" vs. stable policies

## Relevance

This paper directly addresses Gap #21 (skill lifecycle vs. vanilla RL compositional emergence threshold) from the representational angle: RL Post-Training (Aug 6) showed vanilla RL discovers compositional strategies; this paper explains *why* — RL training restructures internal representations toward more hierarchical, linearly separable structures that support more reliable correctness prediction. The hierarchical deepening of layer importance in RL models is a mechanistic complement to SFT Conflicts/RL Coexists's (Aug 5) gradient-level explanation: where the Aug 5 paper explained why RL gradients are near-orthogonal (variance-limited by advantage normalization), this paper explains what those gradients actually do to the representations.

## My Thoughts

<!-- Add your own notes here -->
