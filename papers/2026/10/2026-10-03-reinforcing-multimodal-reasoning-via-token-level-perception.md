---
title: "Reinforcing Multimodal Reasoning via Token-Level Perception-Grounded Advantage Estimation"
authors: ["Zhihan Zhang", "Lizi Liao"]
date: 2026-09-30
arxiv_id: "2609.39168"
url: "https://arxiv.org/abs/2609.39168"
score: 0.84
topics: [multimodal models, vision language models, VLM, RLHF]
status: unread
---

# Reinforcing Multimodal Reasoning via Token-Level Perception-Grounded Advantage Estimation

## Summary

TPAE addresses coarse sequence-level reward signals in multimodal RL by defining two token-level metrics — visual dependency (how much a token relies on image features) and predictive entropy — and identifying pivotal tokens as statistical outliers in the joint dependency-entropy distribution of correct rollouts. TPAE modulates the sequence-level advantage by each token's statistical consistency with the correct-rollout pattern, producing a fine-grained supervision signal without requiring separate process reward models. Outperforms strong baselines on 7 multimodal benchmarks with more stable and efficient optimization.

## Key Contributions

- Shows empirically that correct reasoning chains exhibit sharper entropy reduction as visual grounding intensifies, compared to incorrect chains
- Pivotal tokens — those whose misprediction triggers reasoning collapse — are statistical outliers in the joint (visual-dependency, predictive-entropy) distribution of correct rollouts
- TPAE weights each token's contribution to the advantage update by its statistical consistency with correct-rollout patterns
- No auxiliary reward model or human annotation required; the statistics come from the model's own correct rollouts

## Relevance

Directly extends the VLM RL thread opened by HaPRL. Where HaPRL uses human-annotated process supervision, TPAE derives fine-grained credit from the model's own correct-rollout statistics — an intrinsic, annotation-free approach. The visual-dependency metric also connects to RFPO's no-gold-labels reward cluster: both use model-internal signals (frozen critic posteriors in RFPO; attention-derived visual dependency in TPAE) to assign credit without external annotation.

## My Thoughts

<!-- Add your own notes here -->
