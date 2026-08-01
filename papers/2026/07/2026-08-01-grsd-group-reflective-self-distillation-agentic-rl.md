---
title: "Group-Reflective Self-Distillation for Agentic Reinforcement Learning"
authors: ["Binbin Zheng", "Zijun Xie", "Guanqun Zhao", "Enlei Gong", "Xing Ma", "Xiaoliang Fu", "Zeyu Chen"]
date: 2026-07-30
arxiv_id: "2607.28076"
url: "https://arxiv.org/abs/2607.28076"
score: 0.84
topics: [agentic RL, GRPO, LLM agent, RLAIF]
status: unread
---

# Group-Reflective Self-Distillation for Agentic Reinforcement Learning

## Summary

GRSD derives capability-aligned, outcome-discriminative guidance from the policy's own verified rollouts: for each prompt, the policy reflects on each trajectory in the on-policy group, and a stop-gradient snapshot contrasts reflections from successful vs. failed trajectories to produce group-level privileged guidance. A self-teacher conditions on this guidance to refine turn-level credit assignment by modulating outcome-based advantages while preserving the verifier's learning direction. Requires no external model—guidance is generated entirely within-group from the policy's own on-policy rollouts.

## Key Contributions

- **Within-group contrastive reflection**: policy generates natural-language reflections on each trajectory in the verified rollout group, then contrasts successful vs. failed reflections to extract what distinguishes winning from losing behaviors at this capability level
- **Stop-gradient snapshot**: the contrastive guidance snapshot is held fixed during the current optimization step, preventing the guidance from creating a moving target during gradient updates
- **Self-teacher advantage modulation**: a self-teacher conditioned on group-level guidance modulates turn-level outcome advantages, providing richer process supervision without external annotation
- Outperforms competitive agentic RL baselines across multiple environments and model scales with better generalization to unseen tasks

## Relevance

Introduces a new structural approach to Gap #16 not represented in the six prior approaches (Dark Room, RDPO, P-GRPO/EmoAgent-R1, CIGPO, OC-GRPO, TAO-RL): rather than modifying the reward signal or filtering groups, GRSD uses within-group reflection contrastive analysis to generate turn-level process supervision from outcome signals — connecting the agentic RL self-distillation thread (Self-Distilled Agentic RL, May 2026) to the credit assignment thread via group-level privileged guidance.

## My Thoughts

<!-- Add your own notes here -->
