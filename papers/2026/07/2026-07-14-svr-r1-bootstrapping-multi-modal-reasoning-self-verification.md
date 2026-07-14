---
title: "SVR-R1: Bootstrapping Multi-modal Reasoning with Self-verification in Reinforcement Learning"
authors: ["Mingyuan Wu", "Jingcheng Yang", "Shengyi Qian", "Xudong Wang", "Jize Jiang", "Qifan Wang", "Aashu Singh", "Khoi Pham", "Fei Liu", "Zhaolun Su", "Zhuokai Zhao", "Klara Nahrstedt", "Jianyu Wang", "Hanchao Yu"]
date: 2026-07-13
arxiv_id: "2607.10966"
url: "https://arxiv.org/abs/2607.10966"
score: 0.88
topics: [multimodal models, vision language models, agentic RL, RL training, GRPO, VLM]
status: unread
---

# SVR-R1: Bootstrapping Multi-modal Reasoning with Self-verification in Reinforcement Learning

## Summary

SVR-R1 introduces a multi-turn GRPO framework for multimodal reasoning in which the model acts as its own verifier, issuing a binary self-verdict (Yes/No) after each answer and triggering a second-chance rethink on 'No' before computing the outcome reward. The framework uses an asynchronous multi-turn rollout design with no external supervision or auxiliary critics. Training dynamics show that verification reliance decreases over time, indicating the model internalizes self-correction as generation and verification capabilities co-evolve via RL.

## Key Contributions

- Binary self-verdict mechanism (Yes/No) triggers a second-chance rethink without external supervision or auxiliary critics
- GRPO + asynchronous multi-turn rollout framework applied to multimodal (vision-language) reasoning
- Training dynamics insight: verification turn count decreases as policy improves, showing internalization of self-correction ability
- Bridges inference-time self-refinement and RL training specifically for VLMs

## Relevance

SVR-R1 directly extends the PAG/Tango verifier co-training thread (vault Jul 13) to the multimodal domain: the same model serves as both policy and verifier (like PAG), verification is binary and triggers regeneration on failure (like PAG's selective revision), and training is GRPO multi-turn (like Turn-Level Reward Jul 13). The decreasing-reliance training dynamic is the VLM counterpart of Tango's co-evolution insight: as RL progresses, the policy internalizes corrections, narrowing the gap between verification and generation capability.

## My Thoughts

<!-- Add your own notes here -->
