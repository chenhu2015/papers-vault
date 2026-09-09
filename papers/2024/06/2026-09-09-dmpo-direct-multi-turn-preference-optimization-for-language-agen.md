---
title: "Direct Multi-Turn Preference Optimization for Language Agents"
authors: ["Wentao Shi", "Mengqi Yuan", "Junkang Wu", "Qifan Wang", "Fuli Feng"]
date: 2026-09-09
arxiv_id: "2406.14868v5"
url: "http://arxiv.org/abs/2406.14868v5"
score: 0.73
topics: [agentic RL, LLM agent, RL training, RLHF]
status: unread
---

# Direct Multi-Turn Preference Optimization for Language Agents

## Summary

DMPO extends DPO to multi-turn language agent tasks by replacing the policy constraint with a state-action occupancy measure constraint in the RL objective, which eliminates the partition function cancellation problem that prevents standard DPO from applying to multi-turn settings. Length normalization is added to the Bradley-Terry model to address disparities between preferred and dispreferred trajectories. Experiments across three multi-turn agent datasets confirm DMPO's effectiveness over standard DPO and online RL baselines.

## Key Contributions

- Identifies the root cause of DPO's failure in multi-turn settings: the partition function does not cancel across turns because it depends on the current state
- Replaces policy constraint with state-action occupancy measure constraint, making the optimization tractable for multi-turn trajectories
- Adds length normalization to Bradley-Terry model to handle trajectory length disparities
- Validated on three multi-turn agent task datasets; outperforms standard DPO and online RL baselines

## Relevance

Provides the theoretical grounding for offline preference learning in multi-turn agentic settings — directly relevant to the Agentic-DPO open gap (Sep 08: offline preference as alternative to GRPO for VLM RL without SFT cold-start). DMPO's state-action occupancy measure formulation is the key enabling technique that makes DPO work for multi-turn agents without online rollouts, connecting to the offline vs. on-policy axis identified in the DiaTool-DPO and EvoHarness-RL threads.

## My Thoughts

<!-- Add your own notes here -->
