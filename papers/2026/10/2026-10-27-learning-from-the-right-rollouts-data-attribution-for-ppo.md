---
title: "Learning from the Right Rollouts: Data Attribution for PPO-based LLM Post-Training"
authors: ["Dong Shu", "Denghui Zhang", "Jessica Hullman"]
date: 2026-04-02
arxiv_id: "2604.01597"
url: "https://arxiv.org/abs/2604.01597"
score: 0.85
topics: [reinforcement learning, RL training, PPO, RLHF]
status: unread
---

# Learning from the Right Rollouts: Data Attribution for PPO-based LLM Post-Training

## Summary

Influence-Guided PPO (I-PPO) integrates data attribution into the PPO post-training loop by computing a gradient-based influence score for each rollout episode and filtering out episodes that are anti-aligned with a validation gradient, rather than training on all generated trajectories indiscriminately. The influence filtering acts as an intrinsic early stopping mechanism, accelerating training while reducing unfaithful chain-of-thought reasoning that would otherwise degrade model performance. I-PPO consistently outperforms both SFT and standard PPO baselines, demonstrating that rollout quality selection is a first-class concern in LLM RL post-training.

## Key Contributions

- Data attribution framework for PPO: per-episode gradient-based influence scoring as a signal for rollout quality
- Filtering criterion: anti-alignment with a validation gradient — a principled alternative to entropy or difficulty proxies
- Intrinsic early stopping: influence filtering naturally terminates training when no more aligned episodes are available
- Reduction in unfaithful CoT reasoning as a by-product of eliminating noisy/anti-aligned trajectories

## Relevance

Complements the RL rollout efficiency cluster (ADS, VIGOR, LEEPS, HIVE, GMTS) from a novel angle: where ADS adapts which data to sample and VIGOR adapts rollout count, I-PPO adapts which sampled rollouts to actually train on via influence attribution. The data-attribution approach is conceptually related to GMTS's gradient-magnitude token selection but applied at the episode level rather than the token level.

## My Thoughts

<!-- Add your own notes here -->
