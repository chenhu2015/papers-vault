---
title: "V-Zero: Answer-Label-Free On-Policy Distillation with Contrastive Evidence Gating for Fine-Grained Visual Reasoning"
authors: ["Haoxiang Sun", "Zhihang Yi", "Langxuan Deng", "Yuhao Zhou", "Peiqi Jia", "Jian Zhao", "Li Yuan", "Jiancheng Lv", "Tao Wang"]
date: 2026-06-24
arxiv_id: "2606.25319v1"
url: "http://arxiv.org/abs/2606.25319v1"
score: 0.78
topics: [multimodal models, vision language models, VLM, RLAIF]
status: unread
---

# V-Zero: Answer-Label-Free On-Policy Distillation with Contrastive Evidence Gating for Fine-Grained Visual Reasoning

## Summary

V-Zero trains VLMs for fine-grained visual reasoning without annotated answer labels. It reframes OPD as negative-free stop-gradient alignment, exposing a ceiling from absent trajectory-level discrimination. To address this, V-Zero pairs a question-relevant regional crop with a negative visual view during training and uses their contrast to gate dense token-level distillation, providing trajectory-level signal without requiring ground-truth answers. Experiments show >5× speedup over SFT methods and >10× over RL baselines with consistent visual reasoning improvements.

## Key Contributions

- Theoretical insight: OPD as negative-free stop-gradient alignment — identifies the absence of trajectory-level discrimination as the structural ceiling for OPD on visual reasoning
- Contrastive evidence gating: question-relevant regional crop paired with a hard negative visual view to evaluate student-sampled trajectories; gating is applied at the token-distillation level
- No answer labels required: replaces answer-verification reward signal (which requires ground truth) with contrastive visual evidence signal
- >5× speedup vs. SFT, >10× vs. RL baselines; consistent gains across multiple visual reasoning benchmarks

## Relevance

V-Zero directly advances the SFT-free VLM RL gap that has been open since Sep 12. ReVisual-R1 (Sep 16) showed that gradient stagnation in multimodal GRPO requires a text-only cold-start but still depends on answer labels; V-Zero removes the label dependency entirely by substituting a contrastive visual evidence signal. The contrastive gating is orthogonal to the NC-GRPO latent diversification approach (Sep 3) — both target VLM rollout quality but NC-GRPO diversifies in latent space while V-Zero gates token-level supervision with a visual contrast signal.

## My Thoughts

<!-- Add your own notes here -->
