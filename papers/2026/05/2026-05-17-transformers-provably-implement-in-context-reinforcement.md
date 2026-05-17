---
title: "Transformers Provably Implement In-Context Reinforcement Learning with Policy Improvement"
authors: ["Haodong Liang", "Lifeng Lai"]
date: 2026-05-07
arxiv_id: "2605.05755"
url: "https://arxiv.org/abs/2605.05755"
score: 0.78
topics: [reinforcement learning, RL training, agentic RL]
status: unread
---

# Transformers Provably Implement In-Context Reinforcement Learning with Policy Improvement

## Summary

This theoretical paper gives explicit parameter constructions proving that a single linear self-attention transformer block can implement semi-gradient SARSA and actor-critic updates, establishing that transformers can execute RL policy improvement algorithms in-context without any weight updates. The work also derives the first convergence guarantee in the in-context RL literature: under sufficient MDP distribution richness, gradient flow converges locally and exponentially to an optimal parameter manifold. Empirical validation on tabular MDPs confirms learned models recover the predicted parameter structure.

## Key Contributions

- Explicit parameter constructions showing linear self-attention implements semi-gradient SARSA and actor-critic in-context
- First convergence guarantee in the ICRL literature: gradient flow converges locally and exponentially under MDP distribution richness conditions
- Teacher-mimicking training procedure with gradient-flow dynamics analysis
- Empirical validation on tabular MDPs confirms constructions are recovered and learned models generalize to unseen MDPs

## Relevance

Provides a mechanistic theoretical foundation for understanding why transformer-based agents trained with RL (as in all the agentic RL papers this digest covers) can internalize and execute RL-like update algorithms. Connects to the broader question of what transformers are actually doing when trained via GRPO/PPO, offering a principled interpretation lens.

## My Thoughts

<!-- Add your own notes here -->
