---
title: "PATS: Policy-Aware Training Scaffolding for Agentic Reinforcement Learning"
authors: ["Yipeng Shi", "Zhipeng Ma", "Yue Wang", "Qitai Tan", "Yang Li", "Peng Chen", "Zhengzhou Zhu"]
date: 2026-07-23
arxiv_id: "2607.21419v1"
url: "http://arxiv.org/abs/2607.21419v1"
score: 0.84
topics: [agentic RL, RL training, LLM agent, tool use]
status: unread
---

# PATS: Policy-Aware Training Scaffolding for Agentic Reinforcement Learning

## Summary

PATS converts rollout groups from the current policy into evidence cards and uses task-specific evaluation to adapt the context provided to subsequent rollouts, giving weak policies concrete guidance on challenging tasks. As the policy improves, redundant scaffolding is revised or removed to reduce reliance on explicit guidance while preserving rollout variation; the scaffold is entirely discarded at deployment with no inference cost. PATS improves over strong baselines by up to 18.6% on ALFWorld and WebShop while using 32.1% fewer prompt tokens on search-augmented QA benchmarks.

## Key Contributions

- Evidence cards: rollout group → natural-language context summarizing patterns observed from current policy's trajectories, injected into subsequent rollout prompts
- Task-specific evaluation drives scaffold adaptation: cards are revised or removed as policy performance improves on each task
- Zero deployment cost: scaffold exists only during training; inference harness unchanged (orthogonal to OpenForgeRL's harness-proxy approach)
- Dual benefit: scaffolding helps weak policies explore effectively while reducing prompt length as policy matures (+18.6% ALFWorld, -32.1% tokens on QA)

## Relevance

Partially closes gap #15 (harness/training-context and RL trainability). OpenForgeRL (Jul 24) established that harness design affects RL trainability; PATS offers a complementary remediation: not by changing the harness architecture but by adapting the training-time context dynamically. The evidence-card mechanism is structurally similar to hindsight relabeling (SEED, today) but operates at the rollout-group prompt level rather than the distillation loss level — both convert completed trajectories into training-time guidance, but PATS injects it as context while SEED injects it as auxiliary loss signal. The progressive removal of scaffolding as policy improves is also related to PATS as a form of capability-sensitive curriculum: it allocates scaffolding budget where the policy most needs it.

## My Thoughts

<!-- Add your own notes here -->
