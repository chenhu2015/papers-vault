---
title: "Visual sensitivity is not claim retractability: persistence-aware credit assignment for multimodal reinforcement learning"
authors: ["Zhongan Bi", "Kepeng Lin", "Xuanang Gao", "Yuhan Sun", "Lianrun Zhang"]
date: 2026-10-04
arxiv_id: "2609.36572"
url: "https://arxiv.org/abs/2609.36572"
score: 0.86
topics: [multimodal models, vision language models, VLM, RLAIF, reward model]
status: unread
---

# Visual sensitivity is not claim retractability: persistence-aware credit assignment for multimodal reinforcement learning

## Summary

This paper separates two VLM properties conflated by outcome-level RLVR: Evidence-Function Sensitivity (EFS — whether predictions change under image intervention) and claim retractability (whether visual claims are actually supported by the image). A fixed-rollout counterfactual diagnostic re-scores the same response under an intervened image to reveal that 27.81% of correctly-answered responses contain unsupported visual claims that inherit positive credit from the correct outcome. Persistence-aware credit assignment down-weights high-persistence claims (those that survive image intervention, indicating unsupported grounding) to correct this structural misattribution.

## Key Contributions

- EFS vs. claim retractability distinction: sensitivity to image changes ≠ claims actually being supported
- Fixed-rollout counterfactual diagnostic: re-scores the same response under an intervened image without re-sampling the model
- 27.81% baseline: fraction of correctly-answered responses containing at least one unsupported direct visual claim in Qwen2.5-VL-7B
- Persistence-aware credit assignment as a structural correction to outcome-level RLVR for multimodal models

## Relevance

This paper directly extends the no-gold-labels credit cluster (CCS + cross-attention RL + TGPO PRM + RFPO + TPAE) to the VLM credit-assignment problem from a grounding-fidelity angle. TPAE identified pivotal tokens via visual-dependency + predictive entropy; this paper takes the complementary approach: identifying which visual claims survive image intervention (persistent = unsupported) and down-weighting them. Together, TPAE and this paper define two complementary axes of VLM credit correction: importance (TPAE) vs. verifiability (this paper).

## My Thoughts

<!-- Add your own notes here -->
