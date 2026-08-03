---
title: "Don't Mix Rewards, Mix Policies: Policy Decomposition and Optimization for Multi-Reward RL"
authors: ["Ruiming Liang", "Yi Zhong", "Yizhen Yuan", "Yinan Zheng", "Tianyi Tan", "Tianyue Wang", "Haiyun Guo", "Jinqiao Wang", "Xianyuan Zhan"]
date: 2026-08-03
arxiv_id: "2607.29246"
url: "http://arxiv.org/abs/2607.29246v1"
score: 0.79
topics: [RLHF, RLAIF, RL training, reinforcement learning, tool use, LLM agent]
status: unread
---

# Don't Mix Rewards, Mix Policies: Policy Decomposition and Optimization for Multi-Reward RL

## Summary

PRISM decomposes multi-reward LLM RL into separate standalone positive policies (one per reward dimension) plus a shared global negative policy, rather than compositing conflicting reward signals. This avoids gradient conflict between objectives during training while enabling flexible policy composition at inference time for per-dimension preference control. Experiments on scientific reasoning, tool-use reasoning, and helpfulness-safety alignment show PRISM consistently outperforms multi-reward RL baselines.

## Key Contributions

- Reformulates multi-reward RL as policy-space decomposition: one positive policy per reward + one shared negative policy
- Training avoids reward gradient conflict by keeping reward-specific policies separate
- Inference-time composition enables controllable preference weighting across reward dimensions
- Evaluated on three diverse settings: scientific reasoning, tool-use reasoning, helpfulness-safety alignment

## Relevance

PRISM addresses a gap in the vault's RL training literature: all prior papers optimize a single reward (or a fixed scalarized combination). PRISM's policy decomposition approach is directly relevant to the user's interests in tool use and agentic RL, where an agent must simultaneously satisfy correctness, tool selection, and format constraints—three naturally conflicting reward signals. The positive/negative policy structure is related to GOPO's ordinal reward transformation (both address multi-signal conflicts in GRPO), but PRISM operates at the architecture level (separate policies) rather than the reward normalization level.

## My Thoughts

<!-- Add your own notes here -->
