---
title: "Reward Models Are Secretly Value Functions: Temporally Coherent Reward Modeling"
authors: ["Alex Nikulkov"]
date: 2026-04-24
arxiv_id: "2604.22981"
url: "https://arxiv.org/abs/2604.22981"
score: 0.84
topics: [reward model, RLHF, RL training]
status: unread
---

# Reward Models Are Secretly Value Functions: Temporally Coherent Reward Modeling

## Summary

TCRM regularizes reward models with Monte Carlo and TD objectives so that each token position outputs the conditional expectation of the final reward, directly connecting reward modeling to RL value functions without architectural changes. This yields interpretable token-level reward trajectories (middle-token accuracy improves from 50% to 88.9%), state-of-the-art PRM performance on ProcessBench from outcome data alone, and unified reward/value modeling in PPO reducing peak GPU memory 27%.

## Key Contributions

- Two regularization terms (MC and TD objectives) added on top of Bradley-Terry loss; minimizers are provably equal to conditional expected rewards at each token
- Unified reward/value modeling in PPO: eliminates separate value network, reducing peak GPU memory 27% and step time 19% with matching quality
- State-of-the-art PRM performance on ProcessBench (44.9% F1) among models trained only on outcome data — no CoT step annotations required
- Token-level reward trajectories become interpretable: mid-token pairwise accuracy rises from 50% (random) to 88.9% while final-token accuracy is preserved

## Relevance

Directly closes the TD-credit side of Gap #6 (TD credit + entropy gating synthesis): where Gated-BEPO applies empirical Bellman backup from rollout graphs, TCRM applies MC+TD regularization to make reward model outputs equal conditional value estimates at every token, establishing a formal bridge between reward models and RL value functions. The unified reward/value model in PPO is a practical instantiation of the same Gap #6 synthesis goal.

## My Thoughts

<!-- Add your own notes here -->
