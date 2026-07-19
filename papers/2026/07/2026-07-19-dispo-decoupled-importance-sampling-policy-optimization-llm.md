---
title: "DISPO: Enhancing Training Efficiency and Stability in Reinforcement Learning for Large Language Model Mathematical Reasoning"
authors: ["Batuhan K. Karaman", "Aditya Rawal", "Suhaila Shakiah", "Mohammad Ghavamzadeh", "Mingyi Hong", "Arijit Biswas", "Ruida Zhou"]
date: 2026-02-01
arxiv_id: "2602.00983"
url: "https://arxiv.org/abs/2602.00983"
score: 0.80
topics: [RL training, agentic RL, PPO, GRPO, reward model, RLHF]
status: unread
---

# DISPO: Enhancing Training Efficiency and Stability in Reinforcement Learning for Large Language Model Mathematical Reasoning

## Summary

DISPO identifies that REINFORCE-style RL methods clip importance sampling weights uniformly for correct and incorrect responses, creating a problematic coupling: for correct responses, weights >1 increase entropy (exploration) and weights <1 increase distillation, while for incorrect responses, over-restriction in either direction triggers catastrophic failures via repetitive outputs or vanishing response lengths. The fix decouples up-clipping and down-clipping of importance sampling weights separately for correct and incorrect responses, yielding four independently tunable policy update regimes. DISPO achieves 61.04% on AIME'24 versus 55.42% for CISPO and 50.21% for DAPO.

## Key Contributions

- Failure mode analysis: characterizes how uniform clipping of importance sampling weights couples four distinct update regimes (correct/incorrect × up-clip/down-clip) with conflicting optimal values
- Decoupled clipping: introduces separate hyperparameters for up/down clipping of correct and incorrect response weights, making all four regimes independently controllable
- Ablation insight for correct responses: weights >1 increase average token entropy (exploration), weights <1 increase distillation — both useful, but excessive application of either causes gradual performance degradation
- Ablation insight for incorrect responses: over-restriction triggers sudden catastrophic failure (repetitive outputs when weight>1 is clamped too low; vanishing lengths when weight<1 is clamped too low)
- 61.04% on AIME'24 vs. 55.42% CISPO, 50.21% DAPO; similar gains across models and benchmarks

## Relevance

Extends the vault's RL optimization internals thread with a new dimension: the asymmetry between correct and incorrect response gradient treatment. Where RIPO fixed the geometric manifold for policy updates and RL-ZVP recovered zero-variance prompts, DISPO fixes the coupling between four update regimes that existing clipping strategies conflate. Together these three papers characterize three orthogonal axes of PPO/GRPO algorithmic deficiency: manifold geometry (RIPO), data coverage (RL-ZVP), and response-type update decoupling (DISPO).

## My Thoughts

<!-- Add your own notes here -->
