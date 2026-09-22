---
title: "ACLArena: Agent Continue Learning in Multi-stage Post-training"
authors: ["Haixin Wang", "Xiaoxuan Wang", "Junkai Zhang"]
date: 2026-09-21
arxiv_id: "2609.23989v1"
url: "https://arxiv.org/abs/2609.23989"
score: 0.79
topics: [agentic RL, RL training, RLHF, agentic]
status: unread
---

# ACLArena: Agent Continue Learning in Multi-stage Post-training

## Summary

ACLArena provides the first systematic framework for Agent Continual Learning (ACL), analyzing forgetting and generalization at both model and token levels across multi-stage training pipelines. It compares multi-teacher on-policy distillation, self-distilled fine-tuning, and model merging, then proposes a new recipe combining offline replay over high-quality trajectories with a routed network of LoRA experts each specialized via RL. Evaluated on four reasoning and agentic tasks in both in-domain and out-of-domain settings.

## Key Contributions

- First systematic study of Agent Continual Learning with analysis of forgetting and generalization at model level (weight plasticity/stability) and token level (distribution shift)
- Benchmarks three integration paradigms: multi-teacher OPD, self-distilled fine-tuning, and model merging — with detailed trade-off analysis
- Proposes an ACL recipe: offline trajectory replay + routed multi-LoRA network where each expert is RL-specialized per capability domain
- Open framework (ACLArena) for reproducible evaluation of ACL approaches across in-domain and out-of-domain settings

## Relevance

Addresses the HarnessBandit gap from a different axis: HarnessBandit schedules which harness to train on within a single session; ACLArena asks how to train across sequential capability stages without forgetting. Together they frame a full multi-capability agent training design space (sequential acquisition + online scheduling). The multi-LoRA + RL recipe is complementary to the joint co-training approach in CoSkill.

## My Thoughts

<!-- Add your own notes here -->
