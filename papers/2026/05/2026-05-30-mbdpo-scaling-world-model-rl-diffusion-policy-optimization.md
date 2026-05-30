---
title: "Scaling World-Model Reinforcement Learning Through Diffusion Policy Optimization"
authors: ["Xiaoyuan Cheng", "Wenxuan Yuan", "Zhancun Mu", "Yuanzhao Zhang", "Yiming Yang", "Hai Wang", "Zhuo Sun", "Che Liu"]
date: 2026-05-25
arxiv_id: "2605.26282"
url: "http://arxiv.org/abs/2605.26282v1"
score: 0.82
topics: [reinforcement learning, RL training]
status: unread
---

# Scaling World-Model Reinforcement Learning Through Diffusion Policy Optimization

## Summary

MBDPO reformulates policy optimization in world models as a diffusion process over searched trajectories in latent space, extracting an implicit energy function from collected data that anchors the policy — eliminating the structural misalignment between search and value learning that limits existing approaches. Evaluated across offline pretraining, online learning, and offline-to-online fine-tuning, MBDPO shows consistent monotonic scaling gains with model capacity on large-scale datasets.

## Key Contributions

- Structural misalignment between search and value learning in world model RL identified as core bottleneck
- MBDPO unifies search and policy optimization via diffusion over searched trajectories in latent space
- Implicit energy function extracted from collected data anchors the policy without explicit planner
- Monotonic performance scaling with model capacity in offline pretraining regime

## Relevance

Covers the unexplored world model / model-based RL angle targeted today — a fresh perspective on scaling RL through differentiating the search-value alignment problem; may inform future LLM planning approaches.

## My Thoughts

<!-- Add your own notes here -->
