---
title: "Data-dependent Exploration for Online Reinforcement Learning from Human Feedback"
authors: ["Zhen-Yu Zhang", "Yuting Tang", "Jiandong Zhang", "Lanjihong Ma", "Masashi Sugiyama"]
date: 2026-05-06
arxiv_id: "2605.04477"
url: "https://arxiv.org/abs/2605.04477"
score: 0.82
topics: [RLHF, reinforcement learning, RL training]
status: unread
---

# Data-dependent Exploration for Online Reinforcement Learning from Human Feedback

## Summary

DEPO (Data-Dependent Exploration for Preference Optimisation) addresses the exploration bottleneck in online RLHF by constructing a history-based uncertainty bonus that steers the policy toward under-explored, potentially high-value regions without needing reliable on-policy estimates. Theoretical regret bounds adapt to task hardness, and DEPO consistently outperforms strong baselines across preference-learning benchmarks.

## Key Contributions

- Identifies the core failure mode of on-policy exploration bonuses in online RLHF: unreliable estimates from limited historical data cause premature down-weighting of under-explored regions
- DEPO: computes uncertainty bonus from historical preference data (off-policy), not on-policy expectations, sidestepping the estimation problem
- Data-dependent regret bound that adapts to task hardness and is tighter than worst-case bounds in practice
- Consistent outperformance over strong baselines; simple and scalable design

## Relevance

Directly addresses the RLHF exploration problem that underpins the online training methods (PPO, GRPO, RLAIF) covered throughout the digest. Complements the exploration strategies thread (PolicySplit, HeRL, DEEP-GRPO) but focuses specifically on the preference-learning / RLHF setting rather than outcome-based RL.

## My Thoughts

<!-- Add your own notes here -->
