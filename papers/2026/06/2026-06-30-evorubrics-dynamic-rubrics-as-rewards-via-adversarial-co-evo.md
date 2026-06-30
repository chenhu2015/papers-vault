---
title: "EvoRubrics: Dynamic Rubrics as Rewards via Adversarial Co-Evolution for LLM Reinforcement Learning"
authors: ["Hongxin Ding", "Baixiang Huang", "Yue Fang", "Weibin Liao", "Zheng Li", "Jinyang Zhang", "Zhijing Wu", "Junfeng Zhao", "Yasha Wang"]
date: 2026-06-30
arxiv_id: "2606.23038"
url: "http://arxiv.org/abs/2606.23038v1"
score: 0.84
topics: [agentic RL, RL training, reward model, GRPO]
status: unread
---

# EvoRubrics: Dynamic Rubrics as Rewards via Adversarial Co-Evolution for LLM Reinforcement Learning

## Summary

Static rubric-based rewards for open-ended RL lose discriminative power as the policy improves, causing reward saturation and hacking — EvoRubrics addresses this via adversarial co-evolution where a Policy LLM and a Rubric Generator jointly update each training step, with the rubric generator adapting criteria in real time to remain discriminative as the policy improves. This co-evolution naturally induces an automatic curriculum without external supervision, and the learned rubric generator generalizes as a transferable reward model. Even a fully self-supervised variant (no external supervision) achieves meaningful gains, suggesting co-evolution between generation and evaluation alone provides sufficient learning signal.

## Key Contributions

- Adversarial co-evolutionary RL framework: policy and rubric generator update jointly within each training step
- Rubric generator adapts criteria in real time to remain discriminative as policy improves, inducing automatic curriculum
- Self-supervised variant requires no external supervision or ground truth — co-evolution itself provides the signal
- Learned rubric generator transfers as a standalone reward model for new tasks

## Relevance

EvoRubrics is the dynamic complement to the static rubric pipeline built in Jun 19 (ARES for offline rubric synthesis, ARBOR for online rubric accumulation): where ARES generates rubrics once from pretraining data and ARBOR accumulates rubrics online, EvoRubrics makes the rubric generator itself a trainable adversary that stays ahead of the policy. The "saturation and hacking" diagnosis is the rubric-level version of the reward hacking thread (PRIME/HARVE/Preference Instability Jun 17-18): fixed rubrics Goodhart just as fixed reward models do, and adversarial co-evolution is the structural solution.

## My Thoughts

<!-- Add your own notes here -->
