---
title: "E3-Orch: Towards Effective, Efficient, and Extensible Agentic Orchestration with Reinforcement Learning"
authors: ["Junnan Liu", "Linhao Luo", "Thuy-Trang Vu", "Gholamreza Haffari"]
date: 2026-08-05
arxiv_id: "2608.04588"
url: "https://arxiv.org/abs/2608.04588"
score: 0.78
topics: [agentic RL, RL training, LLM agent, agentic]
status: unread
---

# E3-Orch: Towards Effective, Efficient, and Extensible Agentic Orchestration with Reinforcement Learning

## Summary

E3-Orch trains a reinforcement learning-based orchestrator for multi-agent systems using a milestone-plan-act workflow, where milestones provide a mid-level abstraction that scopes planning around meaningful intermediate objectives. Fine-grained credit assignment operates at the milestone and plan levels via tree-structured rollouts comparing alternative decisions under shared execution histories, with complementary rewards optimizing task performance, execution cost, and planning completeness. The learned orchestration policy transfers to unseen executor configurations at evaluation time.

## Key Contributions

- Milestone-plan-act workflow: milestones scope planning around intermediate objectives, enabling adaptive re-planning as execution progresses
- Tree-structured rollouts comparing alternative milestone/plan decisions under shared execution histories for fine-grained credit assignment
- Complementary reward functions covering task performance, execution cost, planning completeness, and uncertainty-aware performance for stochastic outcomes
- Policy transfers to unseen executor configurations, supporting extensible orchestration without retraining

## Relevance

E3-Orch sits at the intersection of multi-agent orchestration and agentic RL, complementing the single-policy agentic RL cluster (SAGE-OPD, EMPO, SERO, RIPPLE) with a multi-agent perspective. Its milestone-level credit assignment mechanism is distinct from token-level or trajectory-level credit assignment seen elsewhere, and the tree-structured rollout comparison is a novel training signal design for orchestration tasks.

## My Thoughts

<!-- Add your own notes here -->
