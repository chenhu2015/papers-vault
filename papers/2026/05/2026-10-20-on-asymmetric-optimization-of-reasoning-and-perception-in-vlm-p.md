---
title: "On Asymmetric Optimization of Reasoning and Perception in Vision-Language Model Post-Training"
authors: ["Xueqing Wu", "Yu-Chi Lin", "Kai-Wei Chang", "Nanyun Peng"]
date: 2026-05-28
arxiv_id: "2605.29496"
url: "https://arxiv.org/abs/2605.29496"
score: 0.79
topics: [multimodal models, vision-language, VLM, RLHF, reward model]
status: unread
---

# On Asymmetric Optimization of Reasoning and Perception in Vision-Language Model Post-Training

## Summary

Diagnoses two root causes of perception-reasoning asymmetry in VLM post-training: token imbalance in SFT (perception occupies fewer chain-of-thought tokens, so reweighting loss boosts end-to-end performance by up to 18.2 points) and reward coupling in RL (outcome rewards correlate more strongly with reasoning than perception). Adding a perception-aware reward to RL improves end-to-end accuracy by up to 6.0 points; a surrogate perception reward yields 2.2 points when ground-truth is unavailable.

## Key Contributions

- Controlled diagnostic framework with two synthetic tasks that isolate perception from reasoning in VLM post-training
- Two distinct mechanisms for asymmetry: token imbalance (SFT) vs. reward coupling (RL)
- SFT fix: loss reweighting toward perception tokens (+18.2 pp end-to-end)
- RL fix: perception-aware reward term (+6.0 pp), with a reliable surrogate when GT unavailable (+2.2 pp)

## Relevance

Provides a complementary diagnostic angle to PARA/GRAD (Oct 19): where PARA identifies perception-headroom vs. reasoning-headroom bottlenecks and GRAD uses attention distillation to address them, this paper identifies the training-objective mechanisms (token imbalance, reward coupling) causing the bottleneck and provides direct fixes at the loss/reward level. Together, these papers form a complete diagnosis-and-fix framework for VLM RL credit imbalance.

## My Thoughts

<!-- Add your own notes here -->
