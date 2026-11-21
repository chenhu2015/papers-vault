---
title: "Athena: Enhancing Multimodal Reasoning with Data-efficient Process Reward Models"
authors: ["Shuai Wang", "Zhenhua Liu", "Jiaheng Wei", "Xuanwu Yin", "Dong Li", "Emad Barsoum"]
date: 2025-06-11
arxiv_id: "2506.09532"
url: "https://arxiv.org/abs/2506.09532"
score: 0.82
topics: [reward model, multimodal models, VLM, vision-language models, RLHF]
status: unread
---

# Athena: Enhancing Multimodal Reasoning with Data-efficient Process Reward Models

## Summary

Athena-PRM is a data-efficient multimodal process reward model that uses prediction consistency between weak and strong completers to automatically generate step-level annotations, requiring only 5,000 samples. It achieves SOTA on VisualProcessBench (+3.9 F1) and boosts test-time scaling by 10.2 points on WeMath with Qwen2.5-VL-7B, with additional gains from ORM initialization and up-sampling of negative data.

## Key Contributions

- Prediction consistency criterion: a step label is reliable when weak and strong completers agree, avoiding noisy Monte Carlo estimation
- ORM initialization for PRM training: initializes from an outcome reward model to accelerate convergence and stabilize step-level scoring
- Up-sampling of negative data to address the severe class imbalance in process labels
- Three-scenario evaluation: test-time scaling verification, direct step correctness assessment, and reward-ranked fine-tuning (Athena-7B)

## Relevance

This is the first PRM paper to surface via search after four failed attempts using "process reward model" vocabulary — it was found via the adaptive reasoning thread, not PRM vocabulary. The multimodal PRM gap has been an open thread since Nov 16; Athena-PRM closes it with a data-efficient approach using consistency labeling rather than Monte Carlo, which is notably cheaper and more applicable to VLM settings.

## My Thoughts

<!-- Add your own notes here -->
