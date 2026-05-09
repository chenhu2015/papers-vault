---
title: "Uncertainty-Aware Exploratory Direct Preference Optimization for Multimodal Large Language Models"
authors: ["Huatian Zhang", "Zhendong Mao", "Lei Zhang", "Yongdong Zhang"]
date: 2026-05-09
arxiv_id: "2605.04874v1"
url: "http://arxiv.org/abs/2605.04874v1"
score: 0.82
topics: [RLHF, VLM, multimodal, vision-language]
status: unread
---

# Uncertainty-Aware Exploratory Direct Preference Optimization for Multimodal Large Language Models

## Summary

UE-DPO proposes an uncertainty-aware DPO variant for multimodal LLMs that quantifies token-level epistemic uncertainty from the model's failure to ground visual token predictions in the input image. Using this uncertainty signal, the method applies more learning pressure on visually deficient tokens in preferred outputs while alleviating over-penalization in dispreferred samples. This self-referential bias correction consistently reduces hallucination across VLM benchmarks with theoretical justification.

## Key Contributions

- Identifies self-referential bias in existing DPO for VLMs: sensitivity estimated by a model still under training reinforces already well-learned visual cues
- Proposes token-level epistemic uncertainty quantified from grounding failures as a training signal
- Uncertainty-aware exploration intensity differentially weights preferred vs. dispreferred sample gradients
- Theoretical justification of the uncertainty-aware reweighting plus consistent empirical improvements

## Relevance

This is the first paper in the digest to directly target DPO for VLMs — a gap given the strong RLHF/multimodal overlap in the interest profile. The epistemic uncertainty angle complements prior reward model quality papers (TraceLift, Power Distribution) by addressing alignment fidelity at the token level rather than the rollout level.

## My Thoughts

<!-- Add your own notes here -->
