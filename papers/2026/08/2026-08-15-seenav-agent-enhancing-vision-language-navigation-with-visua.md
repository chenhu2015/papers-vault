---
title: "SeeNav-Agent: Enhancing Vision-Language Navigation with Visual Prompt and Step-Level Policy Optimization"
authors: ["Zhengcheng Wang", "Zichuan Lin", "Yijun Yang", "Haobo Fu", "Deheng Ye"]
date: 2026-08-15
arxiv_id: "2512.02631"
url: "http://arxiv.org/abs/2512.02631v1"
score: 0.72
topics: [vision-language, VLM, multimodal, GRPO, reward model, RL training]
status: unread
---

# SeeNav-Agent: Enhancing Vision-Language Navigation with Visual Prompt and Step-Level Policy Optimization

## Summary

SeeNav-Agent introduces SRGPO (Step Reward Group Policy Optimization) for vision-language navigation: verifiable process rewards are defined per navigation step, and step-level advantages are estimated by randomly grouping navigation steps rather than rolling out full trajectories. SRGPO provides dense step-level RL signals for VLN post-training, improving training stability and convergence over GRPO and GiGPO, while a dual-view visual prompt module addresses spatial perception hallucinations. Qwen2.5-VL-3B with SRGPO post-training reaches 72.3% navigation success rate, outperforming the best existing LVLM by 5.6 pp.

## Key Contributions

- Defines verifiable process rewards for each navigation step using VLN task structure
- SRGPO: step-level group relative advantage estimation by randomly grouping steps within a trajectory — applies GRPO's group-relative principle at step granularity rather than rollout granularity
- Dual-view visual prompt (VP) module reduces spatial hallucinations without additional training
- 72.3% success rate with 3B model, outperforming larger models trained with GRPO/GiGPO

## Relevance

SRGPO's random step grouping applies the "group relative" principle one level down from GRPO: where GRPO groups rollouts to compute relative advantages, SRGPO groups steps within a rollout. This complements Temporal GRPO (Aug 14) which groups rollouts within the same task stage — together they define a three-level hierarchy: step-group (SRGPO) → stage-group (Temporal GRPO) → rollout-group (standard GRPO). The verifiable step reward definition for VLN connects to the verifiable process supervision thread (VPS, VPRM, VERDICT) and to CSO's critical step verification — both use task-structure-derived verifiability to avoid noisy step-level reward estimation.

## My Thoughts

<!-- Add your own notes here -->
