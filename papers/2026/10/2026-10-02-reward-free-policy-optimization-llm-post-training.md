---
title: "Unlocking the Critic: Reward-Free Policy Optimization for LLM Post-Training"
authors: ["Hongyang Li", "Xiao Li", "Caesar Wu", "Said Mammar", "Grégoire Danoy", "Pascal Bouvry"]
date: 2026-09-29
arxiv_id: "2609.37119v1"
url: "http://arxiv.org/abs/2609.37119v1"
score: 0.85
topics: [agentic RL, RL training, reward model, RLHF, LLM agent]
status: unread
---

# Unlocking the Critic: Reward-Free Policy Optimization for LLM Post-Training

## Summary

RFPO repurposes a single pretrained, frozen critic as a rollout-level reward signal, a value baseline for GAE, and a success forecaster for incomplete prefixes — eliminating the need for reward labels in the training loop entirely. Binarizing the debiased critic score prevents length-bias exploitation, and the method matches supervised PPO at reduced compute and memory cost. Its ability to reward unfinished prefixes makes it well-suited for long-horizon reasoning where outcomes arrive late.

## Key Contributions

- Frozen pretrained critic used simultaneously as reward, GAE baseline, and prefix-level success forecaster — three roles from one model, no label needed at training time
- Binarization of the debiased critic output prevents the policy from exploiting length bias in the critic's predictions
- Matches supervised PPO on long chain-of-thought reasoning without a single reward label in the training loop
- Rewarding unfinished prefixes eliminates the need to wait for trajectory completion, reducing generation overhead

## Relevance

This is a fourth entry in the no-gold-labels reward design space alongside CCS (cycle-consistency), cross-attention RL (attention fidelity), and TGPO PRM (subgoal progress). RFPO's mechanism is qualitatively different: instead of a proxy derived from task structure or model internals, it leverages a separately trained value model's posterior predictions. Key open question: does a "calibrated frozen critic" presuppose the same annotated data that the method claims to eliminate — or is the critic itself trained with only verifiable rewards?

## My Thoughts

<!-- Add your own notes here -->
