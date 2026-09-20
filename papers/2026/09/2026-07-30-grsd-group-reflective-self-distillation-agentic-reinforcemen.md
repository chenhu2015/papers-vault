---
title: "Group-Reflective Self-Distillation for Agentic Reinforcement Learning"
authors: ["Binbin Zheng", "Zijun Xie", "Guanqun Zhao", "Enlei Gong", "Xing Ma", "Xiaoliang Fu", "Zeyu Chen"]
date: 2026-07-30
arxiv_id: "2607.28076v2"
url: "http://arxiv.org/abs/2607.28076v2"
score: 0.82
topics: [agentic RL, GRPO, RL training, reward model, RLAIF]
status: unread
---

# Group-Reflective Self-Distillation for Agentic Reinforcement Learning

## Summary

GRSD derives group-level privileged guidance from the policy's own verified on-policy rollouts rather than an external teacher. For each prompt, a stop-gradient policy snapshot reflects on each trajectory in the group and contrasts reflections from successful vs failed rollouts to construct capability-aligned guidance; a self-teacher conditioned on this guidance modulates outcome-based advantages per turn while preserving verifier-determined direction. Experiments across multiple agentic environments and model scales show consistent improvement over self-distillation baselines and better generalization to unseen tasks.

## Key Contributions

- Group-level reflection: policy reflects on each trajectory in an on-policy group rather than a single trajectory or external teacher corpus
- Stop-gradient snapshot ensures the reflection is grounded in the policy's current capability distribution, avoiding mismatch
- Outcome-discriminative guidance construction: contrasts successful vs failed rollout reflections to isolate capability-aligned signals
- Turn-level credit modulation: self-teacher adjusts per-turn advantages while preserving the verifier-determined outcome direction

## Relevance

Addresses the inter-trajectory comparison axis that BATON's Trajectory Mass Normalization (TMN) identifies but from a content/reflection angle rather than a mass normalization angle. Where BATON equalizes trajectory mass across the group, GRSD extracts contrastive content signals from the group. Together they define a two-axis inter-trajectory space (mass equalization × contrastive content) that is still unstudied jointly. Found via TMN/inter-trajectory weighting search (Sep 20).

## My Thoughts

<!-- Add your own notes here -->
