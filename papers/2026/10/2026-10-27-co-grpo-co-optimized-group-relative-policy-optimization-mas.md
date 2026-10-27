---
title: "Co-GRPO: Co-Optimized Group Relative Policy Optimization for Masked Diffusion Model"
authors: ["Renping Zhou", "Zanlin Ni", "Tianyi Chen", "Zeyu Liu", "Yang Yue", "Yulin Wang", "Yuxuan Wang", "Jingshu Liu", "Gao Huang"]
date: 2025-12-25
arxiv_id: "2512.22288"
url: "https://arxiv.org/abs/2512.22288"
score: 0.74
topics: [multimodal models, reinforcement learning, GRPO]
status: unread
---

# Co-GRPO: Co-Optimized Group Relative Policy Optimization for Masked Diffusion Model

## Summary

Co-GRPO reformulates Masked Diffusion Model (MDM) generation as a unified MDP that simultaneously captures both model parameters and inference schedule parameters, then applies trajectory-level GRPO to cooperatively optimise both under a shared reward without requiring backpropagation through the multi-step denoising process. This addresses the fundamental training/inference discrepancy in MDMs, where single-step BERT-style training never optimises the multi-step token-decoding trajectory that governs inference. Results on four benchmarks (ImageReward, HPS, GenEval, DPG-Bench) across language and cross-modal generation demonstrate state-of-the-art generation quality.

## Key Contributions

- Unification of model parameters and inference schedule into a single MDP — first to jointly optimise both in MDMs
- Trajectory-level GRPO applied to MDMs, avoiding costly multi-step backpropagation
- Cooperative optimisation: model and schedule share the same reward signal and update simultaneously
- Validated across language and cross-modal generation tasks on 4 benchmarks

## Relevance

Extends the diffusion LM RL cluster (7 entries) with a trajectory-level GRPO application to Masked Diffusion Models specifically, addressing the discrete token prediction setting. Complements UDM-GRPO (seen Oct 26, 0.78) which targeted text-domain discrete diffusion; Co-GRPO targets the MDM architecture variant used in cross-modal generation. Together these two papers populate the discrete/masked diffusion RL sub-cluster.

## My Thoughts

<!-- Add your own notes here -->
