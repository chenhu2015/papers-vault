---
title: "SkillScaffold: Scaffolding Agentic Reinforcement Learning with Policy-Adaptive Skill Credit Assignment and Selective Injection"
authors: ["Wenlin Zhong", "Hao Wang", "Kun Yuan", "Fan Yang", "Jinluan Yang", "Dian Jin", "Xu Tan", "Yiquan Wu", "Kun Kuang"]
date: 2026-10-13
arxiv_id: "2610.18807v1"
url: "https://arxiv.org/abs/2610.18807"
score: 0.86
topics: [agentic RL, LLM agent, reinforcement learning, RLVR, agentic]
status: unread
---

# SkillScaffold: Scaffolding Agentic Reinforcement Learning with Policy-Adaptive Skill Credit Assignment and Selective Injection

## Summary

SkillScaffold estimates per-skill utility via outcome-aware likelihood comparisons on already-collected training trajectories, avoiding expensive rollout-based probing. It injects skills selectively — abstaining when no candidate is estimated to help — and trains a Generator jointly with the Executor to keep skills aligned to the evolving policy. Shows consistent gains over strong agentic-RL and skill-based baselines on ALFWorld, WebShop, ScienceWorld, and τ²-Bench.

## Key Contributions

- Outcome-aware likelihood comparison as a cheap proxy for rollout-based skill utility estimation
- Selective skill injection with abstention when no skill is expected to help
- Joint Generator–Executor training keeps skill library adapted to current policy competence
- Skill internalization during training enables skill-free inference at test time

## Relevance

Extends the AutoScaffold/JoMoHa cluster with a qualitatively different mechanism: rather than a frozen teacher (AutoScaffold) or joint harness co-training (JoMoHa), SkillScaffold builds a dynamic skill library with policy-adaptive credit assignment. The abstention mechanism directly addresses the over-injection failure mode that prior skill-based RL methods suffer from, and is the first to close the loop between skill utility estimation and training trajectory reuse.

## My Thoughts

<!-- Add your own notes here -->
