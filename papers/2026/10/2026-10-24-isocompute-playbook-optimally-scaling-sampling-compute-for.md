---
title: "IsoCompute Playbook: Optimally Scaling Sampling Compute for LLM RL"
authors: ["Zhoujun Cheng", "Yutao Xie", "Yuxiao Qu", "Amrith Setlur", "Shibo Hao", "Varad Pimpalkhute", "Tongtong Liang", "Feng Yao", "Zhengzhong Liu", "Eric Xing", "Virginia Smith", "Ruslan Salakhutdinov", "Zhiting Hu", "Taylor Killian", "Aviral Kumar"]
date: 2026-03-12
arxiv_id: "2603.12151v1"
url: "http://arxiv.org/abs/2603.12151v1"
score: 0.85
topics: [RL training, GRPO, reinforcement learning, reward model]
status: unread
---

# IsoCompute Playbook: Optimally Scaling Sampling Compute for LLM RL

## Summary

Proposes a compute-optimal framework for allocating sampling budget in on-policy LLM RL post-training, showing that optimal parallel rollouts per problem increase predictably before saturating—driven by solution sharpening on easy problems and coverage expansion on hard problems. Increasing rollouts reduces inter-problem interference, while batch size primarily affects stability and can vary widely. Provides prescriptive scaling rules validated across base models and data distributions.

## Key Contributions

- Identifies compute-optimal rollout count as a function of budget, characterizing the saturation pattern across easy vs. hard problems via two distinct mechanisms (sharpening vs. coverage)
- Shows increasing parallel rollouts mitigates inter-problem interference, while batch size affects stability but within a broad acceptable range
- Validates prescriptive allocation rules across base models and data distributions, recasting RL scaling laws as actionable resource planning tools
- Directly connects to the "How RL Reshapes LLM Reasoning" paper's coverage/sharpening dichotomy with practical allocation rules

## Relevance

Directly extends the RL training dynamics/scaling thread opened by "How RL Reshapes LLM Reasoning" and Ring-Zero, providing the first prescriptive compute allocation rules for on-policy LLM RL post-training. The sharpening/coverage framing mirrors the strategy redistribution analysis in "How RL Reshapes," tying theoretical RL compute scaling to practical engineering choices.

## My Thoughts

<!-- Add your own notes here -->
