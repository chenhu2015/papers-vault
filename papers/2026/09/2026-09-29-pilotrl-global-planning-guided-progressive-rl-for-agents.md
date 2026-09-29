---
title: "PilotRL: Training Language Model Agents via Global Planning-Guided Progressive Reinforcement Learning"
authors: ["Keer Lu", "Chong Chen", "Bin Cui", "Yunhuai Liu", "Wentao Zhang"]
date: 2026-09-29
arxiv_id: "2508.00344v5"
url: "https://arxiv.org/abs/2508.00344"
score: 0.78
topics: [agentic RL, RL training, LLM agent, agentic]
status: unread
---

# PilotRL: Training Language Model Agents via Global Planning-Guided Progressive Reinforcement Learning

## Summary

PilotRL introduces AdaPlan, an adaptive global plan-based agent paradigm that conditions execution on an explicit high-level plan, then trains via a three-stage progressive RL curriculum: (1) supervised imitation to learn plan-following, (2) RL to optimise plan quality, (3) joint optimisation of planner and executor together. This decouples strategy formation from step-level execution in a principled training schedule rather than requiring them to emerge together. LLaMA-3.1-8B + PilotRL surpasses GPT-4o by 3.60% on agent benchmarks and GPT-4o-mini by 55.78%.

## Key Contributions

- AdaPlan paradigm: explicit global plan conditions all downstream action execution, enabling long-horizon strategic guidance beyond ReAct's single-step reasoning
- Three-stage progressive training: imitation → plan-optimising RL → joint planner+executor RL, avoiding instability of training both simultaneously
- 8B open model surpassing GPT-4o on agent benchmarks via structured curriculum
- Addresses ReAct's limitation of purely reactive step-by-step execution without global intent

## Relevance

Complements StraTA (2026-09-28) in the strategy-conditioned agentic RL thread: StraTA samples a compact strategy token at rollout time within GRPO, while PilotRL conditions on an explicit global plan via a staged curriculum. Both validate the hypothesis that explicit high-level guidance improves agentic RL, but use different mechanisms — StraTA's diversity sampling vs. PilotRL's progressive decoupled training. Together they cover the space of how to inject planning structure into agentic RL.

## My Thoughts

<!-- Add your own notes here -->
