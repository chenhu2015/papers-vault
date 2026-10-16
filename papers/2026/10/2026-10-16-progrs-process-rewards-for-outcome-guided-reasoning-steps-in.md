---
title: "Process Rewards for Outcome-Guided Reasoning Steps in LLM Reinforcement Learning"
authors: ["Mohammad Rezaei", "Jens Lehmann", "Sahar Vahdati"]
date: 2026-10-16
arxiv_id: "2604.02341"
url: "https://arxiv.org/abs/2604.02341"
score: 0.80
topics: [reinforcement learning, reward model, GRPO, RLHF, PPO]
status: unread
---

# Process Rewards for Outcome-Guided Reasoning Steps in LLM Reinforcement Learning

## Summary

PROGRS treats PRM scores as relative preferences within outcome groups rather than absolute targets, introducing outcome-conditioned centering that shifts PRM scores of incorrect trajectories to zero mean per prompt group, removing systematic bias while preserving informative rankings. A multi-scale coherence evaluator is integrated into GRPO without auxiliary objectives or additional trainable components. Across MATH-500, AMC, AIME, MinervaMath, and OlympiadBench, PROGRS consistently improves Pass@1 over outcome-only baselines with fewer rollouts.

## Key Contributions

- Outcome-conditioned centering: shifts PRM scores of incorrect-outcome trajectories to zero mean within each prompt group, preventing "fluent failure" reward hacking
- Frozen quantile-regression PRM combined with multi-scale coherence evaluator as the process signal source
- Integrates into GRPO without auxiliary objectives or extra trainable parameters
- Consistent improvements on five math reasoning benchmarks (MATH-500, AMC, AIME, MinervaMath, OlympiadBench) with fewer rollouts

## Relevance

PROGRS addresses the reward hacking / bias problem that arises when PRM scores are treated as absolute rewards in GRPO — directly complementing PASS (found today) which addresses the advantage construction side. Together these two papers provide a complete picture of safe PRM integration into GRPO: PROGRS debiases the signal, PASS shapes how it accumulates into advantages.

## My Thoughts

<!-- Add your own notes here -->
