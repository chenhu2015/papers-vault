---
title: "MOPD: Multi-Teacher On-Policy Distillation for Capability Integration in LLM Post-Training"
authors: ["Wenhan Ma", "Jianyu Wei", "Liang Zhao", "Hailin Zhang", "Bangjun Xiao", "Lei Li", "Qibin Yang", "Bofei Gao", "Yudong Wang", "Rang Li", "Jinhao Dong", "Zhifang Sui", "Fuli Luo"]
date: 2026-07-05
arxiv_id: "2606.30406"
url: "https://arxiv.org/abs/2606.30406"
score: 0.75
topics: [RL training, LLM agent, GRPO, agentic RL]
status: unread
---

# MOPD: Multi-Teacher On-Policy Distillation for Capability Integration in LLM Post-Training

## Summary

MOPD integrates multiple RL-trained capabilities into a single LLM by running per-domain specialized RL to produce domain teachers, then distilling them into a student on the student's own rollouts — eliminating exposure bias while providing a dense optimization signal. On Qwen3-30B-A3B it outperforms Mix-RL, Cascade RL, Off-Policy Finetune, and Param-Merge baselines, and was deployed in MiMo-V2-Flash at frontier scale, demonstrating that the on-policy rollout bridge enables independent parallel development of domain teachers.

## Key Contributions

- MOPD paradigm: per-domain RL teachers → on-policy rollout bridge → student distillation, eliminating exposure bias
- Outperforms Mix-RL, Cascade RL, Off-Policy Finetune, and Param-Merge on Qwen3-30B-A3B
- Enables parallel, independent domain teacher development — removes cross-domain coupling
- Deployed in MiMo-V2-Flash at industrial frontier scale

## Relevance

MOPD extends the on-policy distillation thread (GTR-Turbo Jul 2, CRAFT Jul 2) from single-teacher to multi-teacher scenarios. Where GTR-Turbo used a merged RL checkpoint as a free teacher, MOPD inverts the relationship: specialized domain teachers distill into a generalist student via the student's own rollouts. The on-policy rollout bridge is structurally the same mechanism CRAFT uses for sibling-rollout counterfactuals — both exploit the fact that the student's own trajectories provide an on-distribution distillation target.

## My Thoughts

<!-- Add your own notes here -->
