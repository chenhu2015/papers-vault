---
title: "RefCritic: Training Long Chain-of-Thought Critic Models with Refinement Feedback"
authors: ["Qiaoyu Tang", "Hao Xiang", "Le Yu", "Bowen Yu", "Hongyu Lin", "Yaojie Lu", "Xianpei Han", "Le Sun", "Junyang Lin"]
date: 2026-06-07
arxiv_id: "2507.15024v1"
url: "http://arxiv.org/abs/2507.15024v1"
score: 0.79
topics: [RLHF, reward model, RL training, reinforcement learning, PPO]
status: unread
---

# RefCritic: Training Long Chain-of-Thought Critic Models with Refinement Feedback

## Summary

RefCritic shows that SFT-trained critic modules produce superficial critiques that fail to genuinely improve model reasoning; instead it trains a long-CoT critic via RL with dual rule-based rewards: instance-level solution-judgment correctness and refinement accuracy of the policy model given the critique. On Qwen2.5-14B and DeepSeek-R1-Distill-Qwen-14B across five benchmarks, RefCritic achieves +6.8%/+7.2% AIME25 gains and outperforms step-level supervised critics on ProcessBench despite being trained only with solution-level supervision.

## Key Contributions

- Diagnosis: SFT-based critic modules produce superficial critiques with insufficient reflection and verification
- Dual RL reward: instance-level correctness of solution judgments + refinement accuracy of the policy model guided by critiques
- RefCritic on Qwen2.5-14B: +6.8% on AIME25; on DeepSeek-R1-Distill-Qwen-14B: +7.2% on AIME25
- Outperforms step-level supervised approaches on ProcessBench without step-level training supervision

## Relevance

Extends the critic/value estimation thread from June 1 (POISE/DARE/ReCrit) but specifically focuses on training critic models via RL rather than just using them. The dual reward design — incorporating both judgment accuracy and refinement quality — is a novel angle on reward model objectives that connects to the RM-NLHF paper's argument for richer process signals over binary classification.

## My Thoughts

<!-- Add your own notes here -->
