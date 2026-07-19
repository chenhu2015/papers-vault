---
title: "SD-MAR: Multi-image Analytical Reasoning via Synthetic Data and Reinforcement Learning"
authors: ["Shiyu Yuan", "Sourav Sanjukta Bhabesh", "Zhe Wang", "Dmitriy Bespalov", "Wesley Rose", "Huzefa Rangwala"]
date: 2026-07-15
arxiv_id: "2607.14333"
url: "https://arxiv.org/abs/2607.14333"
score: 0.83
topics: [multimodal models, vision language models, agentic RL, GRPO, reward model]
status: unread
---

# SD-MAR: Multi-image Analytical Reasoning via Synthetic Data and Reinforcement Learning

## Summary

SD-MAR introduces a synthetic data framework for training VLMs on multi-image analytical reasoning tasks (change detection, quantitative comparison, semantic attribution) via controlled visual perturbations. The key RL contribution is GRPO-lite with Backward Discounted Allocation (BDA), which removes KL regularization and upweights credit toward later reasoning steps where analytical conclusions form, exploiting the insight that earlier steps are less informative for visual comparison tasks. Qwen2.5-VL-7B fine-tuned on SD-MAR achieves +36.95% in-domain accuracy over baseline while preserving out-of-domain performance on MME and MMMU-Pro.

## Key Contributions

- SD-MAR benchmark/framework: controlled visual perturbations generate paired multi-image scenarios for training and evaluation across semantic change attribution and quantitative comparison
- GRPO-lite: removes KL regularization from standard GRPO to allow stronger policy optimization without conservatism constraints
- Backward Discounted Allocation (BDA): credit allocation scheme that assigns higher advantage weights to later reasoning steps, operationalizing the domain-specific insight that analytical conclusions in multi-image tasks are formed at the end of reasoning chains
- Out-of-domain generalization preserved: within 1% on MME/MMMU-Pro/MathVista while improving up to +4% on MMBench

## Relevance

Directly addresses two core interest profile areas — multimodal/VLM models and RL training — in a single paper. BDA is a novel credit assignment scheme complementary to the vault's token-level (EGRSD, Prune-OPD) and turn-level (TurnOPD) weighting papers, but operating at the reasoning-step level for VLM tasks specifically.

## My Thoughts

<!-- Add your own notes here -->
