---
title: "Replacing Parameters with Preferences: Federated Alignment of Heterogeneous Vision-Language Models"
authors: ["Shule Lu", "Yujing Wang", "Hainan Zhang", "Xiaoshan Yang", "Hongwei Zheng", "Yongxin Tong", "Changsheng Xu", "Zhiming Zheng"]
date: 2026-05-09
arxiv_id: "2605.03426v1"
url: "http://arxiv.org/abs/2605.03426v1"
score: 0.79
topics: [GRPO, reward model, RLHF, VLM, multimodal]
status: unread
---

# Replacing Parameters with Preferences: Federated Alignment of Heterogeneous Vision-Language Models

## Summary

MoR proposes a federated alignment framework that combines GRPO with a Mixture-of-Rewards mechanism for heterogeneous VLMs in privacy-sensitive settings. Each client trains a local reward model from local preference annotations; these are fused via a learned routing mechanism, and the server optimizes a base VLM with GRPO and a KL penalty without requiring shared parameters or raw data. MoR outperforms federated alignment baselines across diverse VLM benchmarks while preserving cross-client adaptability.

## Key Contributions

- Preference-based federated VLM alignment: eliminates need for parameter or data exchange across clients
- Mixture-of-Rewards (MoR) mechanism with learned routing to fuse heterogeneous client reward signals
- GRPO + KL penalty server-side optimization without requiring architecture homogeneity
- Enables privacy-preserving RL alignment for healthcare/finance VLM settings

## Relevance

Novel combination of GRPO (core interest keyword) with reward model ensemble in a federated setting — extends the reward model training thread from May 7 into the multi-client, privacy-constrained regime. The architecture-agnostic reward fusion is a practically important contribution for the VLM alignment space.

## My Thoughts

<!-- Add your own notes here -->
