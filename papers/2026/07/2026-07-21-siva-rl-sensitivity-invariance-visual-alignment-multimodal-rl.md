---
title: "SIVA-RL: Sensitivity-Invariance Visual Alignment for Multimodal Reinforcement Learning"
authors: ["Cheng Tang", "Junzhi Ning", "Min Cen", "Wei Li", "Xinyi Zeng", "Pinxian Zeng", "Rongbin Li", "Qiming Zhu", "Yuqiang Li", "Junjun He", "Yirong Chen", "Ming Hu"]
date: 2026-07-21
arxiv_id: "2607.13931"
url: "https://arxiv.org/abs/2607.13931"
score: 0.87
topics: [multimodal models, vision language models, RL training, GRPO, VLM, reward model, vision-language]
status: unread
---

# SIVA-RL: Sensitivity-Invariance Visual Alignment for Multimodal Reinforcement Learning

## Summary

SIVA-RL addresses the gap between RLVR answer-level correctness and visual evidence grounding by replacing fixed operator-conditioned visual interventions with sample-wise, outcome-conditioned supervision via token-aligned, distance-constrained PatchSwap. A frozen audit policy scores each clean-intervention pair; the observed reward drop becomes soft routing weights — large-drop pairs drive sensitivity alignment, low-drop pairs drive invariance alignment — decoupling intervention construction from supervision assignment. Applied to GRPO and DAPO on Qwen2.5-VL-3B/7B, yields 8.79pp gain on vision-dependent reasoning and up to 14.9% relative overall improvement across nine multimodal reasoning benchmarks.

## Key Contributions

- Identification that existing visual-intervention supervision assigns supervision by operator type rather than observed effect, which fails because identical operators produce heterogeneous outcomes across samples
- PatchSwap: token-aligned, distance-constrained within-image patch intervention that produces localized, controlled visual perturbations
- Frozen audit policy scoring clean-intervention pairs, with observed reward drop converted to soft routing weights (sample-wise outcome-conditioned supervision)
- Dual alignment objective: sensitivity alignment for large-drop pairs (model should attend to the patch region), invariance alignment for low-drop pairs, ambiguous pairs down-weighted

## Relevance

SIVA-RL extends the VLM RL visual faithfulness thread (CORA, FWS) with a supervision mechanism that operates during RL optimization (not as a pre-training warm-start). Its outcome-conditioned routing is the visual analogue to DISPO's decoupled IS weight clipping — both papers replace operator-level policies (DISPO: symmetric clipping for all responses; SIVA-RL: operator-conditioned supervision for all interventions) with sample-wise, outcome-conditioned decisions. Together SIVA-RL and DyCo-RL establish that VLM RL requires both attention-level coordination (DyCo-RL) and sample-level visual grounding supervision (SIVA-RL) beyond what answer-level rewards provide.

## My Thoughts

<!-- Add your own notes here -->
