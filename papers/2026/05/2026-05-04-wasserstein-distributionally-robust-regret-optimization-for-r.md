---
title: "Wasserstein Distributionally Robust Regret Optimization for Reinforcement Learning from Human Feedback"
authors: ["Yikai Wang", "Shang Liu", "Jose Blanchet"]
date: 2026-04-30
arxiv_id: "2605.00155v1"
url: "http://arxiv.org/abs/2605.00155v1"
score: 0.79
topics: [RLHF, reward model, PPO, GRPO, RL training]
status: unread
---

# Wasserstein Distributionally Robust Regret Optimization for Reinforcement Learning from Human Feedback

## Summary

DRRO addresses reward Goodharting in RLHF by pessimising worst-case regret relative to the best policy under plausible reward perturbations, rather than pessimising worst-case value as in standard DRO. Under an L1 Wasserstein ambiguity set, the inner problem admits an exact water-filling policy structure, yielding a PPO/GRPO-compatible algorithm with a simple sampled-bonus interpretation. Experiments show DRRO mitigates reward overoptimisation more effectively than DRO while being systematically less pessimistic, providing a principled fix for proxy reward collapse.

## Key Contributions

- Reframes Goodharting as a decision problem under objective misspecification, solved via distributionally robust regret (not value)
- Proves the inner worst-case regret under L1 Wasserstein ambiguity admits an exact water-filling closed-form policy
- Bayesian optimisation on unlabeled queries finds optimal combination coefficients on the Pareto frontier
- Drop-in replacement for standard PPO/GRPO training: only minor changes to reward computation required

## Relevance

The reward overoptimisation / Goodharting problem is a known concern in RLHF (covered obliquely by Curriculum-RLAIF and the shallow-RLHF gradient analysis paper). DRRO provides the most mathematically principled treatment yet, and its PPO/GRPO compatibility makes it directly applicable to any of the reward model papers already in the vault. The water-filling policy structure is a novel theoretical result for RLHF practitioners.

## My Thoughts

<!-- Add your own notes here -->
