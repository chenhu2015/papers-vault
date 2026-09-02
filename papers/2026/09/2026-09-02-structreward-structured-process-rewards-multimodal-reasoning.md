---
title: "StructReward: Efficient Structured Process Rewards for Self-Correcting Multimodal Reasoning"
authors: ["Yifan Li", "Ruxin Sun", "Tongzhou Zhao"]
date: 2026-08-08
arxiv_id: "2608.08326"
url: "http://arxiv.org/abs/2608.08326v2"
score: 0.83
topics: [GRPO, multimodal, VLM, reward model, RL training]
status: unread
---

# StructReward: Efficient Structured Process Rewards for Self-Correcting Multimodal Reasoning

## Summary

StructReward provides dense RL training signals for multimodal reasoning by representing solutions as step sequences aligned with process-labeled references via lightweight numerical, symbolic, and lexical matching — no separate learned verifier needed. The aligned labels feed a gated GRPO objective combining dense process reward with answer correctness and output validity rewards. Policy rollouts are recycled into reflection-oriented self-correction training, making the overall multimodal RL pipeline substantially more compute-efficient.

## Key Contributions

- Step-sequence alignment against process-labeled references using lightweight matching (numerical, symbolic, lexical) — no neural PRM
- Gated GRPO objective combining dense process reward, final-answer correctness, and output-validity signals
- Rollout recycling: policy rollouts from GRPO updates are repurposed as reflection-oriented self-correction training instances
- A strong LLM rewrites sampled correct trajectories into reflection-oriented data to reinforce reasoning evaluation and refinement

## Relevance

This paper sits at the intersection of three active vault threads: (1) GRPO improvement — MaxPO (Aug 31) and OTB (Sep 01) targeted the advantage estimator and per-token baseline respectively; StructReward targets the reward signal itself by replacing binary outcome reward with dense process reward inside GRPO. (2) Multimodal RL — the VLM/multimodal dimension of the interest profile has been underexplored relative to the RL training thread. (3) Process rewards — CEB (Aug 31) applied hindsight labeling at inference time; StructReward applies it during training, completing the picture.

## My Thoughts

<!-- Add your own notes here -->
