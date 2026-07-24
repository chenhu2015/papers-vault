---
title: "Clip-Low Increases Entropy and Clip-High Decreases Entropy in Reinforcement Learning of Large Language Models"
authors: ["Jaesung R. Park", "Junsu Kim", "Gyeongman Kim", "Jinyoung Jo", "Sean Choi", "Jaewoong Cho", "Ernest K. Ryu"]
date: 2026-07-24
arxiv_id: "2509.26114"
url: "http://arxiv.org/abs/2509.26114v1"
score: 0.85
topics: [RLHF, PPO, GRPO, RL training, reward model]
status: unread
---

# Clip-Low Increases Entropy and Clip-High Decreases Entropy in Reinforcement Learning of Large Language Models

## Summary

This paper provides the first rigorous theoretical and empirical analysis showing that clip-low in PPO/GRPO induces an upward entropy bias while clip-high induces a downward bias; under standard clipping parameters, the clip-high effect dominates, producing net entropy reduction even when rewards are purely random. The finding reveals that entropy collapse in RLVR is confounded by the clipping mechanism itself, independent of the reward signal. Practically, the authors demonstrate that deliberately setting a more aggressive clip-low value can maintain high entropy and prevent entropy collapse during prolonged training.

## Key Contributions

- Theoretical proof that clip-low (suppressing probability-decrease updates) creates upward entropy bias; clip-high (suppressing probability-increase updates) creates downward entropy bias
- Empirical verification that under standard ε=0.2 PPO/GRPO parameters, clip-high dominates → net entropy collapse even under random rewards (no learning signal)
- Demonstration that aggressive clip-low can function as an explicit anti-collapse regularizer, preventing entropy collapse without modifying the reward
- Reframes entropy collapse in RLVR as partly a clipping artifact, not purely a reward-signal phenomenon

## Relevance

This directly closes the Jul 23 queued question about asymmetric clipping as a stabilizer in LLM RL (parallel to GFlowRL's asymmetric flow-gap clipping and DISPO's asymmetric IS clipping). All three papers now characterize an asymmetric bias in their respective gradient mechanisms: DISPO (one-sided IS clipping on negative advantages), GFlowRL (one-sided flow-gap clipping on trajectory deviations), and this paper (clip-low vs. clip-high entropy biases in the PPO trust region). The entropy collapse analysis also connects to the GRPO web agent failure paper (Jul 22): both identify that the optimization mechanism can independently suppress exploration before the reward signal has a chance to improve the policy.

## My Thoughts

<!-- Add your own notes here -->
