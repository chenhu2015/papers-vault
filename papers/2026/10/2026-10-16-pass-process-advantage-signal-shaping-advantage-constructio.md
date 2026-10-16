---
title: "Process Advantage Signal Shaping: Advantage Construction for Process-Supervised Reinforcement Learning in LLM Reasoners"
authors: ["Chao Wang", "Hongtao Tian", "Tao Yang", "Yunsheng Shi", "Ting Yao", "Wenbo Ding"]
date: 2026-10-16
arxiv_id: "2606.29296"
url: "https://arxiv.org/abs/2606.29296"
score: 0.82
topics: [reinforcement learning, GRPO, reward model, RLHF]
status: unread
---

# Process Advantage Signal Shaping: Advantage Construction for Process-Supervised Reinforcement Learning in LLM Reasoners

## Summary

PASS (Process Advantage Signal Shaping) introduces an advantage-construction pipeline for GRPO that combines separate reward-channel normalization, chunk-based credit accumulation, and normalization by remaining chunk count, linking local feedback scale to the resolution and horizon of policy updates. Evaluated on seven math benchmarks and multi-hop QA, PASS improves average pass@1 by 4.62 points over outcome-only GRPO while reducing average response length by ~2%. The design explicitly addresses how dense process supervision should be converted into policy advantages, a gap not addressed by standard GRPO.

## Key Contributions

- Reward-channel normalization that handles multiple process reward signals independently before fusion
- Chunk-based credit accumulation: groups tokens into signal-defined chunks so local feedback contributes at the right resolution and horizon
- Normalization by remaining chunk count, connecting credit scale to the remaining trajectory length
- +4.62 pts average pass@1 on seven math benchmarks over outcome-only GRPO with shorter responses

## Relevance

PASS directly advances the process reward / step-level credit assignment thread that has been a recurring theme across the vault (SHARPO, TRIAGE, ERSR, SPLIT-RL, LVRL). It is the most complete published pipeline for converting dense process supervision into GRPO advantages, complementing PROGRS (found today) which addresses the orthogonal problem of keeping PRM scores outcome-aligned.

## My Thoughts

<!-- Add your own notes here -->
