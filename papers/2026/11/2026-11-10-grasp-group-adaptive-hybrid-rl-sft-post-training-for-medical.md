---
title: "GRASP: Group-Adaptive Hybrid RL-SFT Post-Training for Medical VQA without Reasoning Annotations"
authors: ["Wanqi Dong", "Wanyue Dong", "Jingze Ge", "Mehul Motani"]
date: 2026-10-25
arxiv_id: "2610.34561v1"
url: "https://arxiv.org/abs/2610.34561"
score: 0.72
topics: [RLVR, vision language models, multimodal models, VLM, RLAIF]
status: unread
---

# GRASP: Group-Adaptive Hybrid RL-SFT Post-Training for Medical VQA without Reasoning Annotations

## Summary

GRASP combines RL and SFT in every update using only short answer annotations, with the balance adapting per question to how well the model currently answers: RL lets the model explore its own reasoning while SFT teaches the gold answer to supply direct supervision RL lacks. Training only 1% of parameters with LoRA, GRASP beats all compared objectives in-domain and OOD, outperforming models trained on 2,600× more data across eight imaging modalities — establishing annotation-efficient RLVR for domain-specialized VLM post-training.

## Key Contributions

- Group-adaptive RL-SFT balance: RL dominates when model answers correctly (exploration); SFT with gold answer compensates when it fails (direct supervision)
- No reasoning traces required: works from short answer annotations alone — directly addresses the annotation scarcity problem in specialized domains
- LoRA efficiency: only 1% trainable parameters; tested on Qwen3-VL-8B, InternVL3-8B, Gemma 3-4B
- OOD generalization: beats 10 compared VLMs (medical and general) on 8-modality OOD benchmark, including models with 2,600× more training data

## Relevance

Relevant to the RLVR data efficiency thread (DE-Venus, InSight) and the VLM RL thread. Where DE-Venus addresses active selection + weak supervision in a unified framework for LLMs, GRASP addresses the same annotation efficiency problem for domain-specialized VLMs with an adaptive RL-SFT blending mechanism. The per-question RL-SFT balance based on group correctness is a novel adaptive training signal complementary to DE-Venus's training-time supervision refinement.

## My Thoughts

<!-- Add your own notes here -->
