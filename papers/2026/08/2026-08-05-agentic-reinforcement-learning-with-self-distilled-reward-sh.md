---
title: "Agentic Reinforcement Learning with Self-Distilled Reward Shaping"
authors: ["Ranxu Zhang", "Guinan Chen", "Chenshaodong", "Jinghao Lin", "Xiaozhou Xu", "Sunzhe", "Yanyong Zhang", "Chao Wang"]
date: 2026-08-05
arxiv_id: "2608.03223"
url: "https://arxiv.org/abs/2608.03223"
score: 0.84
topics: [agentic RL, RL training, reward model, LLM agent, GRPO]
status: unread
---

# Agentic Reinforcement Learning with Self-Distilled Reward Shaping

## Summary

ADRS addresses the sparse-reward credit assignment problem in multi-turn agentic RL by using a frozen policy snapshot to rescore tokens from skill-free trajectories, gated by a Teacher Value Advantage (TVA) signal computed from within-group teacher-confidence/return correlation. The TVA gate filters teacher guidance to only apply when it actually predicts outcomes within the current rollout group, while keeping inference and rollout generation skill-free. Experiments across three interactive benchmarks show consistent gains over GRPO baselines across RL backbones, reduced-data settings, and extended training.

## Key Contributions

- Teacher Value Advantage (TVA) gate: modulates frozen-snapshot teacher scores by their within-group confidence-return correlation, filtering teacher signal to where it actually predicts outcomes
- Center-and-normalize step-level teacher scores before TVA modulation, preventing positional bias
- Integration into native RL credit construction while keeping rollouts and inference privilege-free
- Consistent gains across three benchmarks, multiple RL backbones, reduced data, and unseen tasks

## Relevance

ADRS is the second paper today (alongside SPyCE from Aug 3) to close the training-loop between a policy's own past snapshots and its current credit computation. Unlike SPyCE (which co-evolves skill libraries with the multimodal policy), ADRS operates on individual token-level credit within each GRPO step — using the within-group return correlation to gate the teacher, a direct descendant of the TVA/within-group normalization thread running through A²TGPO and PCSD. The TVA gating mechanism is structurally complementary to ADRS companion paper PCSD's persistence-based distillation weights, and together they represent two routes to calibrated teacher credit in agentic RL: confidence-return correlation (ADRS) vs. temporal persistence of teacher advantage (PCSD).

## My Thoughts

<!-- Add your own notes here -->
