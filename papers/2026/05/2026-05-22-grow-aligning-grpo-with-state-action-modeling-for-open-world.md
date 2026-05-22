---
title: "GROW: Aligning GRPO with State-Action Modeling for Open-World VLM Agents"
authors: ["Xiongbin Wu", "Zhihao Luo", "Shanzhe Lei", "Lechao Zhang", "Xuhong Wang", "Jie Yang", "Zhonglong Zheng", "Yuanjie Zheng", "Xin Tan", "Wei Liu"]
date: 2026-05-22
arxiv_id: "2605.20246"
url: "https://arxiv.org/abs/2605.20246"
score: 0.87
topics: [agentic RL, VLM, GRPO, RL training]
status: unread
---

# GROW: Aligning GRPO with State-Action Modeling for Open-World VLM Agents

## Summary

GROW addresses a core bottleneck in multi-turn VLM agent RL: standard GRPO requires full trajectories as training samples, producing excessively long context and noise in open-world tasks. The framework decomposes collected trajectories into state-action samples and computes advantages between these individual samples rather than treating a full trajectory as a single entity, with a surrogate analysis showing the core relative policy optimization signal of GRPO is preserved. Evaluated on 800+ Minecraft tasks, GROW achieves SOTA performance over both inference-time and trained multi-agent baselines.

## Key Contributions

- State-action decomposition of GRPO trajectories: replaces full-trajectory advantage computation with per-state-action advantage, dramatically reducing context length and noise
- Surrogate analysis proving that advantage computation over grouped state-action samples preserves the relative policy optimization signal of GRPO under simplifying assumptions
- SOTA results on 800+ Minecraft open-world tasks over both SFT-based and RL-based multi-agent baselines
- Demonstrates that organizational scaling (larger multi-agent systems) is feasible when grown progressively from smaller trained systems

## Relevance

Directly extends the VLM + GRPO agentic RL thread (VITAL, ICRL, ESearch-R1 from May 20). The key insight — decomposing trajectories into state-action samples — addresses a fundamental scalability problem for applying GRPO to long-horizon multi-turn agents, making this a structural contribution beyond the specific Minecraft domain.

## My Thoughts

<!-- Add your own notes here -->
