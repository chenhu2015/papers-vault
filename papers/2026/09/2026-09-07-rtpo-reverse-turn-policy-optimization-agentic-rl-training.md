---
title: "RTPO: Reverse-Turn Policy Optimization for Stabilizing Agentic RL Training"
authors: ["Yugu Li", "Zehong Cao", "Jianglin Qiao", "Siyi Hu"]
date: 2026-09-07
arxiv_id: "2608.18682v3"
url: "https://arxiv.org/abs/2608.18682"
score: 0.82
topics: [agentic RL, LLM agent, tool use, reinforcement learning, RL training]
status: unread
---

# RTPO: Reverse-Turn Policy Optimization for Stabilizing Agentic RL Training

## Summary

RTPO identifies three tightly coupled instability sources in multi-turn agentic RL — rollout-training context mismatch, weak turn-level credit assignment under sparse terminal rewards, and asynchronous policy drift from short/long trajectory mixing — and traces all three to a common origin in flattened trajectory optimization. It addresses them via a unified reverse-turn formulation that organizes rollouts as sparse reverse trees and performs turn-level updates in temporal reverse order, aligning each decision with its downstream continuation. Experiments show +21.50% over trajectory-level baselines and +10.76% over turn-level baselines on multi-turn agentic RL benchmarks.

## Key Contributions

- Three-instability diagnosis: rollout-training context mismatch, weak turn-level credit, and asynchronous policy drift all share a common structural origin in flattened trajectory optimization
- Reverse-turn formulation: sparse reverse trees + temporal reverse order policy updates; each decision aligned with downstream continuation for causally consistent credit
- On-policy continuation control: prevents asynchronous drift from mixing short/long trajectories under different policy versions
- Theoretical guarantees: eliminates context mismatch and asynchronous drift; reduces credit bias; converges to recursive optimality

## Relevance

RTPO directly advances the agentic RL training stability thread: SINKFLEX-RL (Sep 05) addressed attention-kernel memory infeasibility at long contexts; RTPO addresses the three optimization-level instabilities that appear once memory is solved. The reverse-tree structure is complementary to HARTS (prefix-sharing across rollout trees) — HARTS reduces redundant KV computation, RTPO ensures stable gradient signal through the tree.

## My Thoughts

<!-- Add your own notes here -->
