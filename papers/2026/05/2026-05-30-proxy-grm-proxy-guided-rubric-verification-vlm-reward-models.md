---
title: "Rationale Matters: Learning Transferable Rubrics via Proxy-Guided Critique for VLM Reward Models"
authors: ["Weijie Qiu", "Dai Guan", "Junxin Wang", "Zhihang Li", "Yongbo Gai", "Mengyu Zhou", "Erchao Zhao", "Xiaoxi Jiang", "Guanjun Jiang"]
date: 2026-03-17
arxiv_id: "2603.16600"
url: "http://arxiv.org/abs/2603.16600v2"
score: 0.80
topics: [VLM, reward model, RLHF, vision-language]
status: unread
---

# Rationale Matters: Learning Transferable Rubrics via Proxy-Guided Critique for VLM Reward Models

## Summary

Proxy-GRM trains lightweight proxy agents that predict preference ordering from a candidate rubric alone (without image/response), using their classification accuracy as a rubric-quality reward to train the main VLM generative reward model. With ~50k samples, Proxy-GRM achieves state-of-the-art results on VL-Reward Bench and MM-RLHF-Reward Bench; critically, the learned rubrics transfer to unseen evaluators without additional training.

## Key Contributions

- Proxy-SFT and Proxy-RL agents trained to verify rubric quality via preference-prediction accuracy
- Rubric-quality reward from proxy accuracy provides differentiable training signal for rubric generation
- State-of-the-art on VL-Reward Bench with ~50k samples (4× fewer data than competing methods)
- Learned rubrics transfer to unseen evaluators at test time without retraining

## Relevance

Addresses VLM reward model quality — a key bottleneck for multimodal RLHF — with a transferable rubric approach; complements the multimodal agentic VLM RL thread.

## My Thoughts

<!-- Add your own notes here -->
