---
title: "StraTA: Incentivizing Agentic Reinforcement Learning with Strategic Trajectory Abstraction"
authors: ["Xiangyuan Xue", "Yifan Zhou", "Zidong Wang", "Shengji Tang", "Philip Torr", "Wanli Ouyang", "Lei Bai", "Zhenfei Yin"]
date: 2026-09-28
arxiv_id: "2605.06642v2"
url: "https://arxiv.org/abs/2605.06642"
score: 0.85
topics: [agentic RL, RL training, GRPO, LLM agent, tool use]
status: unread
---

# StraTA: Incentivizing Agentic Reinforcement Learning with Strategic Trajectory Abstraction

## Summary

StraTA introduces an explicit trajectory-level strategy into agentic RL: a compact strategy is sampled from the initial task state, all subsequent actions are conditioned on it, and strategy generation plus action execution are trained jointly via a hierarchical GRPO-style rollout augmented with diverse strategy sampling and critical self-judgment. This breaks the purely reactive limitation of existing GRPO methods by injecting long-horizon intent at rollout time. StraTA reaches 93.1% on ALFWorld, 84.2% on WebShop, and 63.5% on SciWorld, outperforming frontier closed-source models on the latter.

## Key Contributions

- Hierarchical GRPO-style rollout: a compact strategy token prefixes the entire action sequence, decoupling long-horizon planning from step-level execution
- Diverse strategy rollout: K distinct strategies are sampled per task, improving policy exploration beyond standard GRPO's single-trajectory sampling
- Critical self-judgment: the model evaluates its own trajectory quality to weight credit across strategy samples
- Consistent improvement over strong baselines on ALFWorld, WebShop, and SciWorld across model sizes

## Relevance

Directly advances the agentic RL thread; StraTA's hierarchical GRPO rollout is a concrete implementation of the hierarchical structure suggested by ArCHer, applied natively within the GRPO framework without requiring a separate off-policy value function. The diverse strategy sampling angle is a novel complement to the tree rollout design space (EPIG-Tree, Belief-Shift Branching, DATPO) — where those methods vary *branching structure*, StraTA varies *strategy conditioning*.

## My Thoughts

<!-- Add your own notes here -->
