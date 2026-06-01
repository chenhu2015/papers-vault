---
title: "EchoRL: Reinforcement Learning via Rollout Echoing"
authors: ["Jinhe Bi", "Aniri", "Minglai Yang", "Xingcheng Zhou", "Wenke Huang", "Sikuan Yan", "Yujun Wang", "Zixuan Cao", "Michael Färber", "Xun Xiao", "Volker Tresp", "Yunpu Ma"]
date: 2026-06-01
arxiv_id: "2605.31228"
url: "https://arxiv.org/abs/2605.31228"
score: 0.86
topics: [RLVR, GRPO, reward model, LLM agent]
status: unread
---

# EchoRL: Reinforcement Learning via Rollout Echoing

## Summary

EchoRL addresses advantage degeneration in RLVR: when all rollouts for a prompt succeed, advantages become zero and policy gradients vanish, capping training performance. It identifies an EchoClip from verified-success rollouts based on step-level entropy patterns and feeds this clip back as auxiliary supervision in the RL objective. Tested across 10 benchmarks, 5 LLM backbones, and 4 RLVR methods, EchoRL consistently improves training with minimal overhead.

## Key Contributions

- Identifies advantage-degenerated rollouts (all-success prompts) as a systematic training bottleneck in RLVR
- Analyzes entropy patterns in golden trajectories from expert models to understand what makes them informative
- EchoClip selection based on step-level entropy values from verified-success rollouts
- Lightweight auxiliary supervision module compatible with GRPO, DAPO, and other RLVR variants without architecture changes

## Relevance

Advantage degeneration is a natural consequence of successful training (the model learns easy prompts), creating a self-limiting ceiling. EchoRL is complementary to reward design work (like Reward Bias Substitution from May 31) — it addresses the training dynamics problem rather than the reward signal problem.

## My Thoughts

<!-- Add your own notes here -->
