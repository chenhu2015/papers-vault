---
title: "OpenReward: Learning to Reward Long-form Agentic Tasks via Reinforcement Learning"
authors: ["Ziyou Hu", "Zhengliang Shi", "Minghang Zhu", "Haitao Li", "Teng Sun", "Pengjie Ren", "Suzan Verberne", "Zhaochun Ren"]
date: 2025-10-28
arxiv_id: "2510.24636"
url: "https://arxiv.org/abs/2510.24636"
score: 0.76
topics: [GRPO, reward model, LLM agent, agentic, tool use]
status: unread
---

# OpenReward: Learning to Reward Long-form Agentic Tasks via Reinforcement Learning

## Summary

OpenReward introduces OpenRM, a tool-augmented reward model trained with GRPO to judge open-ended long-form responses by dynamically invoking external tools to gather evidence — addressing the limitation of existing reward models on knowledge-intensive tasks where correctness cannot be verified from internal knowledge alone. Trained on 27K synthesized pairwise examples with a joint objective over intermediate tool use and final outcome accuracy, OpenRM substantially outperforms existing reward models at discriminating subtle quality differences. As both an inference-time response selector and training-time data selector, it yields consistent downstream LLM alignment gains.

## Key Contributions

- Tool-augmented reward model: invokes external tools at judgment time to gather evidence for evaluating knowledge-intensive long-form responses
- GRPO training for reward models: applies group relative policy optimization to train the reward model itself, jointly supervising tool invocation and outcome accuracy
- Controllable data synthesis: 27K pairwise examples with structured quality differences for reward model training
- Dual deployment: effective as both inference-time response selector (Best-of-N) and training-time data quality filter

## Relevance

Addresses the DFRL-adjacent shaped reward for LLM agents thread from the Nov 21 digest. DFRL used downstream decision regret as reward for agents; OpenReward goes further by using GRPO to train a reward model that can itself use tools to gather evidence for agentic task evaluation. This is a convergence of the agentic RL and reward model training threads — a reward model that behaves as an agent during evaluation.

## My Thoughts

<!-- Add your own notes here -->
