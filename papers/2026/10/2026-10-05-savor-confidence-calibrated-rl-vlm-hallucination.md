---
title: "SAVOR: Self-Aware Visual Grounding via Confidence-Calibrated Reinforcement Learning for Multimodal Hallucination Mitigation"
authors: ["Zixiu Ding", "Zilin Zhao", "Yingjie He", "Xinlang Kang", "Guansu Wang", "Wei Zhang"]
date: 2026-10-05
arxiv_id: "2609.16601v1"
url: "https://arxiv.org/abs/2609.16601"
score: 0.77
topics: [multimodal models, vision language models, VLM, GRPO, RLHF, reward model]
status: unread
---

# SAVOR: Self-Aware Visual Grounding via Confidence-Calibrated Reinforcement Learning for Multimodal Hallucination Mitigation

## Summary

SAVOR augments VLM outputs with token and answer confidence, then applies GRPO with an objective that penalizes calibration error and poor abstention decisions alongside standard accuracy rewards. At inference time, the learned confidence signal triggers selective visual evidence re-examination only when the model is uncertain, reducing hallucination without the latency cost of universal re-examination. Experiments on POPE, HallusionBench, AMBER, and MMHal-Bench with InternVL3-8B and Qwen3-VL-8B show hallucination reduction with lower Expected Calibration Error than DPO baselines.

## Key Contributions

- Augments output schema with token-level and answer-level confidence fields trained under GRPO
- GRPO objective penalizes calibration error (confidence vs. accuracy gap) and poor abstention decisions, not just answer correctness
- Inference-time selective re-examination: revisits visual evidence only when the learned confidence is below threshold
- Outperforms DPO-variant hallucination baselines on POPE, HallusionBench, AMBER, MMHal-Bench; generalizes across two 8B backbones

## Relevance

SAVOR occupies an interesting position in the VLM RL cluster: it introduces calibrated confidence as a training-time reward component (GRPO penalizes miscalibration), which is related to but distinct from the credit-assignment axes of TPAE (importance), persistence-aware (verifiability), TTRSD (sensitivity), and TTIQ (joint grounding). SAVOR's confidence signal is a 5th axis — *reliability estimation* — that determines when to re-examine visual evidence rather than how to assign credit to specific tokens. The selective re-examination inference mechanism connects to TTRSD's test-time adaptation approach from a different angle.

## My Thoughts

<!-- Add your own notes here -->
