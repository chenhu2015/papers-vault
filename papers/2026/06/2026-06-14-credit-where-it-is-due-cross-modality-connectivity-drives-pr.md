---
title: "Credit Where It is Due: Cross-Modality Connectivity Drives Precise Reinforcement Learning for MLLM Reasoning"
authors: ["Zhengbo Jiao", "Shaobo Wang", "Zifan Zhang", "Wei Wang", "Bing Zhao", "Hu Wei", "Linfeng Zhang"]
date: 2026-06-14
arxiv_id: "2602.11455v1"
url: "http://arxiv.org/abs/2602.11455v1"
score: 0.79
topics: [multimodal models, vision-language, VLM, agentic RL, reward model, RLHF]
status: unread
---

# Credit Where It is Due: Cross-Modality Connectivity Drives Precise Reinforcement Learning for MLLM Reasoning

## Summary

AT-RL identifies that only ~15% of MLLM tokens exhibit strong cross-modal visual-textual connectivity; these anchor tokens are where RLVR credit assignment naturally concentrates during training. Graph-based clustering of attention topology selects high-connectivity anchors for selective reinforcement, while explicitly withholding gradients from low-connectivity tokens — training solely on low-connectivity tokens causes severe degradation, confirming visual anchoring quality governs multimodal reasoning quality. The 32B AT-RL model surpasses the 72B-Instruct baseline on MathVista (80.2) at only 1.2% computational overhead.

## Key Contributions

- Observation: during RLVR training, credit assignment naturally concentrates on ~15% of tokens with high cross-modal visual-textual connectivity — these are the causal locus of multimodal reasoning
- AT-RL: graph-based clustering of attention topology identifies anchor tokens; reinforcement is applied selectively to these; gradients withheld from low-connectivity tokens
- Ablation confirms causality: training on low-connectivity tokens alone causes severe degradation, not just reduced gains
- 32B AT-RL surpasses 72B-Instruct on MathVista (80.2), with consistent gains across STEM, video, and general tasks; 1.2% overhead only

## Relevance

AT-RL bridges the VLM RL thread (VGS/VURB, Jun 9) with the credit assignment thread (PRISM, Reasoning Arena, Jun 13). VGS showed that visual and language objectives have orthogonal gradients in VLMs; AT-RL operationalizes this insight at the token level: rather than reweighting objective components, it identifies the specific tokens where the visual-language binding is strongest and focuses RL credit there.

## My Thoughts

<!-- Add your own notes here -->
