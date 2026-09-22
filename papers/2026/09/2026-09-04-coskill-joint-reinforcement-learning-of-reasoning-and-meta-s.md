---
title: "CoSkill: Joint Reinforcement Learning of Reasoning and Meta-Skill Agents for Hierarchical Skill Evolution"
authors: ["Jinyuan Feng", "Dongmin Li", "Yiqun Chen", "Yang Gao", "Xing Chen", "Huimu Wang", "Zhiqiang Pu"]
date: 2026-09-04
arxiv_id: "2609.04865v2"
url: "https://arxiv.org/abs/2609.04865"
score: 0.90
topics: [agentic RL, RL training, LLM agent]
status: unread
---

# CoSkill: Joint Reinforcement Learning of Reasoning and Meta-Skill Agents for Hierarchical Skill Evolution

## Summary

CoSkill unifies skill evolution and policy optimization by recasting the static meta-skill workflow as a learnable Meta-Skill Agent jointly trained with a Reasoning Agent over a hierarchical skill library. Both agents share a single backbone and co-adapt end-to-end: the Reasoning Agent conditions on retrieved task and step skills while its task performance guides Meta-Skill Agent refinement of those skills. Achieves 98.4% / 90.6% on ALFWorld / WebShop, +3.5 and +6.2 pp over prior skill-based RL baselines with superior sample efficiency.

## Key Contributions

- Recasts the static meta-skill workflow as a learnable Meta-Skill Agent with its own RL training objective, enabling joint co-adaptation with the Reasoning Agent
- Hierarchical skill library organizes knowledge at task and step granularity; retrieval-conditioned Reasoning Agent uses both levels during inference
- Single-backbone shared architecture enables end-to-end co-adaptation without separate training phases
- Demonstrates superior early-stage sample efficiency alongside improved asymptotic performance

## Relevance

Directly advances the ArenaFlow skill memory thread (2026-09-18) by making skill evolution itself learnable and jointly trained rather than a static background process. Also extends APEx's two-level skill store (task memories + procedural skills) by jointly optimizing the skill manager alongside the policy — the gap ArenaFlow identified between skill storage and policy co-adaptation is directly addressed here.

## My Thoughts

<!-- Add your own notes here -->
