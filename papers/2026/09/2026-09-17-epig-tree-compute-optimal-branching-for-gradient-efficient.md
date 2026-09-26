---
title: "EPIG-Tree: Compute-Optimal Branching for Gradient-Efficient Reinforcement Learning"
authors: ["Nikita Khomich", "Leopold Hermansson", "Ido Hakimi"]
date: 2026-09-17
arxiv_id: "2609.20004"
url: "https://arxiv.org/abs/2609.20004"
score: 0.87
topics: [agentic RL, RL training, GRPO, PPO, reward model]
status: unread
---

# EPIG-Tree: Compute-Optimal Branching for Gradient-Efficient Reinforcement Learning

## Summary

EPIG-Tree reformulates tree-based rollout construction in policy-gradient RL as a compute allocation problem, deriving two allocation laws from a law-of-total-variance decomposition: new branches reduce decision-point gradient uncertainty while repeated suffix rollouts reduce continuation uncertainty. The EPIG score allocates branches using already-computed rollouts, weighting by occupancy and score-weighted value uncertainty, without requiring additional environment interactions. In multi-turn Wordle, EPIG achieves a 0.850 win rate versus flat GRPO's 0.790, confirming that gradient-estimation gains transfer to stateful multi-turn settings.

## Key Contributions

- Law-of-total-variance decomposition of the local policy-gradient random variable into decision uncertainty and continuation uncertainty
- Two allocation laws: branch count reduces decision uncertainty; suffix rollout count follows n_e ∝ w_e * ||∇log π|| * σ_e / sqrt(c_e)
- EPIG score allocates branches from already-computed rollouts — no extra environment calls at allocation time
- In multi-turn Wordle, EPIG (0.850) beats flat GRPO (0.790) and entropy branching, with flat GRPO saturating early; token-level credit assignment is the dominant factor in single-turn math

## Relevance

EPIG-Tree addresses a different axis of the GRPO efficiency problem than GRAFT/SALT/ProCredit: rather than how to assign credit within a fixed rollout set, it asks where to place rollouts to maximize gradient quality per compute unit. The multi-turn Wordle result is the clearest evidence that tree rollout structure improves agentic settings, complementing the step-credit line of work.

## My Thoughts

<!-- Add your own notes here -->
