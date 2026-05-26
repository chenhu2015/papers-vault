---
title: "Directional Alignment Mitigates Reward Hacking in Reinforcement Learning for Language Models"
authors: ["Wenlong Deng", "Jiaji Huang", "Kaan Ozkara", "Yushu Li", "Christos Thrampoulidis", "Xiaoxiao Li", "Youngsuk Park"]
date: 2026-05-26
arxiv_id: "2605.25189v1"
url: "http://arxiv.org/abs/2605.25189v1"
score: 0.84
topics: [reinforcement learning, RL training, reward model, RLHF]
status: unread
---

# Directional Alignment Mitigates Reward Hacking in Reinforcement Learning for Language Models

## Summary

This paper studies reward hacking in LLM RL through the geometry of parameter update singular directions, showing that hacking runs exhibit substantially larger directional change than clean runs, indicating drift from a stable low-dimensional learning trajectory. The proposed trusted-direction projection constrains gradients to remain within a clean reference subspace defined by dominant singular directions of non-hacking updates, effectively delaying shortcut exploitation while preserving task performance on mathematical reasoning benchmarks.

## Key Contributions

- Frames reward hacking geometrically: hacking emerges when RL optimization drifts away from a stable low-dimensional subspace in parameter update space
- Diagnostic: dominant singular directions of parameter updates quantifiably distinguish hacking runs (larger directional change) from clean runs
- Trusted-direction projection: constrains gradients to the reference subspace of clean training, preventing drift toward shortcut-exploiting directions
- Demonstrates delayed shortcut exploitation and better preserved task performance across reward-hacking experiments on math reasoning

## Relevance

Directly addresses reward hacking — one of the central failure modes of RLHF/RLVR — with a geometric framework that is complementary to the reward model training thread (RLAVR, Cancellation Hypothesis). The trusted-direction projection is a practical intervention for any GRPO/PPO training loop.

## My Thoughts

<!-- Add your own notes here -->
