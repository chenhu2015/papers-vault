---
title: "Breaking the SFT Plateau: Multimodal Structured Reinforcement Learning for Chart-to-Code Generation"
authors: ["Lei Chen", "Xuanle Zhao", "Zhixiong Zeng", "Jing Huang", "Liming Zheng", "Yufeng Zhong", "Lin Ma"]
date: 2026-09-05
arxiv_id: "2508.13587v2"
url: "http://arxiv.org/abs/2508.13587v2"
score: 0.75
topics: [multimodal models, vision language models, RL training, reward model, multimodal, VLM]
status: unread
---

# Breaking the SFT Plateau: Multimodal Structured Reinforcement Learning for Chart-to-Code Generation

## Summary

MSRL proposes a multi-granularity reward system for VLM RL combining rule-based textual rewards (validating fine-grained code details) with model-based visual rewards (assessing structural similarity between rendered output and ground-truth charts), implemented as a two-stage curriculum — textual rewards first, then visual augmentation. Trained on 3M chart-code pairs from real-world arXiv tables, MSRL breaks the SFT plateau with +6.2% and +9.9% on ChartMimic and ReachQA. This is the first system to empirically combine the StructReward principle (multi-granularity dense feedback) with the VIG principle (visual information as a training signal) in a single RL objective, though applied to chart-to-code rather than general VLM reasoning.

## Key Contributions

- Multi-granularity reward system: rule-based textual rewards (code detail validation) + model-based visual rewards (rendered-vs-ground-truth structural similarity) in one RL training loop
- Two-stage curriculum: Stage 1 optimizes with textual rewards; Stage 2 adds visual reward signals — demonstrating that visual reward needs textual grounding first
- 3M training corpus from real-world arXiv chart-code pairs, addressing synthetic dataset limitations
- +6.2% ChartMimic, +9.9% ReachQA over SFT; outperforms all chart-domain SOTA and competitive with closed-source models

## Relevance

MSRL provides the first empirical combination of StructReward (multi-granularity dense process feedback, Sep 02) and VIG (visual information as training signal, Sep 04) in a working system. The search from Sep 04 (VIG composability with StructReward) predicted this would be an open gap — MSRL demonstrates the combination is tractable and improves performance, though in the chart domain rather than general VLM reasoning. The two-stage curriculum finding (textual rewards first) also aligns with Demystifying RL Post-Training's base-prior finding: the model needs a textual grounding foundation before visual rewards can provide useful signal.

## My Thoughts

<!-- Add your own notes here -->
