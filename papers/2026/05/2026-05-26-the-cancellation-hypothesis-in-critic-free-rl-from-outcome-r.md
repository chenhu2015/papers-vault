---
title: "The Cancellation Hypothesis in Critic-Free RL: From Outcome Rewards to Token Credits"
authors: ["Tianhao Cheng", "Zeyu Huang", "Zihan Qiu", "Yu Cheng", "Edoardo Ponti", "Yinghui Xu", "Ivan Titov", "Zenglin Xu"]
date: 2026-05-26
arxiv_id: "2605.08666v1"
url: "http://arxiv.org/abs/2605.08666v1"
score: 0.87
topics: [RLVR, GRPO, RL training, PPO, reward model]
status: unread
---

# The Cancellation Hypothesis in Critic-Free RL: From Outcome Rewards to Token Credits

## Summary

This paper reveals the token-flipping phenomenon in critic-free RL (GRPO/RLVR): positive and negative rollouts exhibit nearly identical proportions of tokens being probability-boosted or suppressed, because coupled gradient interactions between identical low-confidence tokens produce cancellation effects that implicitly create token-level credit assignment from outcome-level rewards. Two simple batching interventions — query-preserved mini-batching and reward-balanced batching — exploit this principle to consistently improve RLVR training across multiple model scales.

## Key Contributions

- Identifies token-flipping: in critic-free RL, ~equal fractions of tokens are boosted/suppressed regardless of rollout sign — not explained by advantage alone
- Explains via token coupling: gradient interactions between shared low-confidence tokens dominate; cancellation of opposing signals creates hidden credit assignment
- Empirical support: tokens boosted by critic-free RL have consistently higher value than suppressed tokens, regardless of originating rollout
- Two practical interventions: query-preserved mini-batching (encourage cancellation) and reward-balanced batching (preserve cancellation) improve RLVR across scales

## Relevance

Provides a theoretical lens on why GRPO/RLVR works at the token level, directly extending the step-level credit assignment thread (DelTA, PAIR, SRaR, MoCA) to the finer token granularity. The batching interventions are immediately actionable for anyone running GRPO training.

## My Thoughts

<!-- Add your own notes here -->
