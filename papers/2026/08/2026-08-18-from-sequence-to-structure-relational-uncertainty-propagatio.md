---
title: "From Sequence to Structure: Relational Uncertainty Propagation for LLM Agents"
authors: ["Zhengzhao Ma", "Boxi Cao", "Yaojie Lu", "Hongyu Lin", "Xianpei Han"]
date: 2026-08-18
arxiv_id: "2608.16002"
url: "http://arxiv.org/abs/2608.16002v1"
score: 0.79
topics: [agentic RL, LLM agent, agentic evaluation, tool use]
status: unread
---

# From Sequence to Structure: Relational Uncertainty Propagation for LLM Agents

## Summary

RUPA represents an agent's execution history as a directed trajectory graph (reasoning states, tool interactions, environment feedback as nodes; temporal and semantic dependency edges) and propagates uncertainty over this graph to capture how execution risk accumulates across interaction steps. The propagated signal is combined with trajectory-level behavioral features and goal-alignment information to produce a full-trajectory confidence estimate. Evaluated on τ-2, Terminal-Bench-2, and GAIA across six LLMs, RUPA consistently outperforms local-signal UQ baselines, with the largest gains from the graph-propagation step.

## Key Contributions

- RUPA: directed trajectory graph with temporal and semantic dependency edges; propagates uncertainty to capture long-range error accumulation
- Demonstrates that per-step local UQ (token probabilities, predictive entropy) systematically misses failures whose causes originate several steps before the final answer
- Full-trajectory confidence estimate combining propagated uncertainty + behavioral features + goal-alignment information
- Consistent improvement across six LLMs (1.5B–commercial) on three agent benchmarks (τ-2, Terminal-Bench-2, GAIA)

## Relevance

RUPA provides the uncertainty quantification counterpart to the Aug 17 fault attribution papers (OrchestraBench, Layer-Isolated). Where OrchestraBench and LongRCA Bench localise *where* failures originated post-hoc, RUPA quantifies *how much execution risk* is accumulating in real time via graph propagation. The graph structure mirrors the trajectory-level analysis that ASCon (Aug 18 near-miss candidate) uses for attribution, but RUPA applies it to UQ rather than classification. The finding that per-step local signals miss long-range causal failures directly validates the Horizon Gap's core critique of step-isolated evaluation.

## My Thoughts

<!-- Add your own notes here -->
