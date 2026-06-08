---
title: "HARVE: Hacking-Aware Reward-Head Vector Editing for Robust Reward Models"
authors: ["Shuang Liu", "Yuxuan Bo", "Qiuyang Zhao", "Caiyue Huang", "Xiaorong Chen", "Yanguang Liu", "Mengnan Du"]
date: 2026-06-02
arxiv_id: "2606.03131v1"
url: "http://arxiv.org/abs/2606.03131v1"
score: 0.82
topics: [reward model, RLHF, reinforcement learning, agentic RL]
status: unread
---

# HARVE: Hacking-Aware Reward-Head Vector Editing for Robust Reward Models

## Summary

HARVE introduces RewardHackBench (13 reward-hacking patterns across real-world domains) and finds severe failures across 8 reward models. It proposes a training-free fix: identify a multi-directional hacking subspace from residual stream directions using contrastive gold-hacked examples, then directly remove the reward-head component aligned with that subspace — no gradient updates needed. HARVE outperforms fine-tuning baselines and preserves general reward-model capability.

## Key Contributions

- RewardHackBench: 13 reward-hacking patterns spanning high-stakes and general domains, evaluating 8 reward models
- Training-free reward-head editing: identifies hacking subspace from residual stream directions of contrastive examples
- Removes reward-head alignment with the hacking subspace via direct vector arithmetic, avoiding gradient-based fine-tuning
- Reward hacking is better modeled as a multidimensional residual-space structure than isolated surface cues

## Relevance

Directly answers the OCRM runner-up thread from June 7 (off-policy RM correction for overoptimization) from a mechanistic angle: rather than re-training or off-policy correction, HARVE surgically edits the reward head. Connects with the broader reward model robustness thread (RefCritic/RM-NLHF from June 7, SAVE from June 6).

## My Thoughts

<!-- Add your own notes here -->
