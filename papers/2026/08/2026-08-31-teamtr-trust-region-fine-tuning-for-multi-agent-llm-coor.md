---
title: "TeamTR: Trust-Region Fine-Tuning for Multi-Agent LLM Coordination"
authors: ["Yi Xie", "Siao Liu", "Falong Fan", "Yuanqi Yao", "Yue Zhao", "Bo Liu"]
date: 2026-08-31
arxiv_id: "2605.15207"
url: "https://arxiv.org/abs/2605.15207"
score: 0.80
topics: [reinforcement learning, agentic RL, RL training, LLM agent, PPO]
status: unread
---

# TeamTR: Trust-Region Fine-Tuning for Multi-Agent LLM Coordination

## Summary

TeamTR identifies and formalizes compounding occupancy shift in sequential fine-tuning of shared-context multi-LLM teams: updating one agent shifts the team's context distribution, and stale-occupancy evaluation of subsequent updates incurs a penalty scaling quadratically in the number of agents, versus linear under intermediate-occupancy evaluation. TeamTR proposes a trust-region framework that resamples trajectories after each component update with per-agent divergence control, yielding rigorous per-update improvement lower bounds and 7.1% average gains over single-agent and sequential baselines.

## Key Contributions

- Formal characterization of compounding occupancy shift: sequential fine-tuning of N agents on cached rollouts incurs O(N²) evaluation penalty under stale occupancy, reducible to O(N) by intermediate-occupancy resampling
- Trust-region framework with per-agent KL divergence constraints and trajectory resampling after each component update — avoids cached-rollout mismatch
- Rigorous per-update and per-stage improvement lower bounds under the trust-region constraints
- Supports plug-and-play component replacement: individual agents can be swapped for stronger models without full retraining, consistent with SAT's invariance theorem (Aug 29)

## Relevance

TeamTR is the direct follow-on to SAT (Aug 29) in the multi-LLM team training thread. SAT proved that block-coordinate independent updates give monotonic team improvement with plug-and-play invariance; TeamTR identifies the failure mode (occupancy shift) that makes naive sequential fine-tuning break those guarantees and provides the trust-region fix. The O(N²) vs. O(N) penalty gap is the formal explanation for why SAT's resampling discipline was empirically necessary. Together, SAT + TeamTR form a two-paper foundation for multi-LLM team training theory.

## My Thoughts

<!-- Add your own notes here -->
