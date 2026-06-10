---
title: "Reasoning or Memorization? Direction-Aware Diversity Exploration in LLM Reinforcement Learning"
authors: ["Jiangnan Xia", "Yucheng Shi", "Yu Yang", "Kishan Panaganti", "Zhenwen Liang", "Ninghao Liu"]
date: 2026-06-09
arxiv_id: "2606.10346v1"
url: "http://arxiv.org/abs/2606.10346v1"
score: 0.80
topics: [reinforcement learning, RL training, GRPO, agentic RL, reward model]
status: unread
---

# Reasoning or Memorization? Direction-Aware Diversity Exploration in LLM Reinforcement Learning

## Summary

DiRL extracts an internal reasoning-versus-memorization direction from model representations and uses direction-weighted gradient features to characterise each rollout update, shaping GRPO rewards to amplify reasoning-aligned exploration while suppressing memorization-aligned variation. The key insight is that existing diversity bonuses treat novel-seeming trajectories from genuine reasoning and from memorised shortcuts equally, steering exploration toward the wrong mode. DiRL integrates seamlessly into standard GRPO and significantly improves over existing exploration methods on mathematical and general reasoning benchmarks.

## Key Contributions

- Identifies reasoning-memorization direction as a learnable internal signal from model activations
- Direction-weighted gradient features characterise whether a rollout update moves toward reasoning or memorization
- Reward shaping that amplifies reasoning-aligned and suppresses memorization-aligned diversity
- Plug-in for GRPO with no architectural changes; consistent improvements on math and general reasoning

## Relevance

Directly extends the GRPO exploration thread from DiScO (Jun 9, diversity reward over reasoning transitions) but adds a principled mechanistic distinction: DiRL knows *why* a trajectory is diverse, not just that it is. Connects to Tell-Tale Norm (Jun 9) which also uses internal representation signals (l2 norm ↔ SAE features) to detect reasoning quality — DiRL applies the same philosophy to reward shaping rather than test-time steering.

## My Thoughts

<!-- Add your own notes here -->
