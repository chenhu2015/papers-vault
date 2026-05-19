---
title: "Step-wise Rubric Rewards for LLM Reasoning"
authors: ["Weichu Xie", "Haozhe Zhao", "Wenpu Liu", "Yongfu Zhu", "Liang Chen", "Minghao Ye", "Zirong Chen", "Yuqi Xu", "Shuai Dong", "Ziyue Wang", "Xinbo Xu", "Kean Shi", "Ruoyu Wu", "Xiaoying Zhang", "Wenqi Shao", "Baobao Chang", "Nan Duan", "Jiaqi Wang"]
date: 2026-05-17
arxiv_id: "2605.17291v1"
url: "http://arxiv.org/abs/2605.17291v1"
score: 0.83
topics: [reward model, RLHF, RL training, GRPO, PPO]
status: unread
---

# Step-wise Rubric Rewards for LLM Reasoning

## Summary

SRaR identifies that standard rubric-based RL rewards applied uniformly to entire responses cause 18.2% of steps in correct responses to be wrongly penalized and 49.9% of steps in incorrect responses to be wrongly rewarded. It attributes each rubric criterion to a specific reasoning step, normalizes per-step scores across rollouts, and combines step-level with outcome rewards via a decoupled advantage estimator, improving average accuracy by 3.57 points over RaR on Qwen3-8B and reducing self-correction looping from 48.1% to 26.5%.

## Key Contributions

- Quantifies rubric aggregation error: uniform scalar rewards mislabel a large fraction of individual steps even when the overall response scoring is directionally correct
- Step-wise attribution: each rubric criterion is assigned to a specific reasoning step by an LLM judge, enabling targeted per-step supervision
- Cross-rollout normalization of per-step rubric scores so only steps with quality variance produce a learning signal, avoiding reward domination by easy steps
- Decoupled advantage estimator keeps the outcome baseline stable while combining step and outcome signals; builds a 16K-problem rubric dataset via contrastive distillation

## Relevance

Directly extends the process reward model thread (SWE-Shepherd, FormalRewardBench) with a rubric-based step attribution mechanism — a cleaner alternative to Monte Carlo step-level rewards that doesn't require rollout-based estimation. Reduces self-correction looping, which connects to reward hacking issues covered on May 9–10.

## My Thoughts

<!-- Add your own notes here -->
