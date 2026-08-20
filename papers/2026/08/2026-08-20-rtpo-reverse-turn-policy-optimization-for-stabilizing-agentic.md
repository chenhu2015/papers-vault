---
title: "RTPO: Reverse-Turn Policy Optimization for Stabilizing Agentic RL Training"
authors: ["Yugu Li", "Jimmy Cao", "Jianglin Qiao", "Siyi Hu"]
date: 2026-08-19
arxiv_id: "2608.18682"
url: "https://arxiv.org/abs/2608.18682"
score: 0.86
topics: [agentic RL, RL training, tool use, LLM agent]
status: unread
---

# RTPO: Reverse-Turn Policy Optimization for Stabilizing Agentic RL Training

## Summary

Identifies three structurally coupled instability sources in multi-turn agentic RL: rollout-training context mismatch, weak turn-level credit under sparse terminal rewards, and asynchronous policy drift from mixing short and long trajectories — all rooted in flattened trajectory optimization. RTPO organizes rollouts as sparse reverse trees and performs turn-level policy updates in reverse temporal order, ensuring causally consistent credit assignment and on-policy continuation; it improves by +21.5% over trajectory-level baselines and +10.76% over turn-level baselines on multi-turn agentic benchmarks.

## Key Contributions

- Theoretical analysis showing the three instability sources share a single structural root in flattened trajectory optimization
- Sparse reverse tree representation that organizes multi-turn rollouts for causal alignment between each decision and its downstream continuation
- Reverse-order turn-level updates that provide theoretical guarantees: elimination of context mismatch, elimination of asynchronous drift, reduced credit bias, and convergence to recursive optimality
- +21.5% vs. trajectory-level baseline on multi-turn agentic RL benchmarks

## Relevance

RTPO directly addresses multi-turn agentic RL stability — the same challenge that Agent Lightning v1.0 and LEGO-RL tackle from a systems perspective. RTPO provides the algorithm-level fix that the systems papers assume is solved: causally correct credit assignment in multi-turn tool-use trajectories. Together with SkillGate (selector credit starvation) these two papers address complementary credit assignment failures in long-horizon agentic RL.

## My Thoughts

<!-- Add your own notes here -->
