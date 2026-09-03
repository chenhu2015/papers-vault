---
title: "Discriminative Policy Optimization for Token-Level Reward Models"
authors: ["Hongzhan Chen", "Tao Yang", "Shiping Gao", "Ruijun Chen", "Xiaojun Quan", "Hongtao Tian", "Ting Yao"]
date: 2026-09-03
arxiv_id: "2505.23363v1"
url: "http://arxiv.org/abs/2505.23363v1"
score: 0.76
topics: [reward model, PPO, RLHF, RLAIF, reinforcement learning]
status: unread
---

# Discriminative Policy Optimization for Token-Level Reward Models

## Summary

Q-RM decouples reward modeling from language generation by deriving a token-level reward model as a discriminative Q-function learned from preference data, avoiding the instability that arises when generative token probabilities are repurposed as reward scores. The Q-function is proven to explicitly capture token-level Q-values from preference data without requiring fine-grained step-level annotations. Integrated with PPO/REINFORCE, Q-RM improves average Pass@1 on math reasoning by 4–6 points over ORM and PRM baselines while achieving 12x faster convergence than ORM on GSM8K and 11x faster than step-level PRM on MATH.

## Key Contributions

- Q-function Reward Model (Q-RM): token-level reward model derived via discriminative policy optimization, decoupled from language generation
- Theoretical proof that Q-RM learns token-level Q-functions from preference data without fine-grained annotations
- 12x faster convergence than ORM on GSM8K, 11x faster than step-level PRM on MATH — significant training efficiency improvement
- Consistent outperformance across benchmarks when integrated with PPO or REINFORCE

## Relevance

Extends the token-level reward theme from OTB (Sep 01) into the reward model design space. OTB showed that group-based policy gradient baselines ignore within-sequence token heterogeneity; Q-RM shows that generative reward models suffer from a parallel conflict between language generation and discriminative reward assignment at the token level. Together they suggest the same token-level heterogeneity problem appears in both the advantage estimator (OTB) and the reward model (Q-RM), and that separating discriminative from generative objectives is the correct fix on both sides.

## My Thoughts

<!-- Add your own notes here -->
