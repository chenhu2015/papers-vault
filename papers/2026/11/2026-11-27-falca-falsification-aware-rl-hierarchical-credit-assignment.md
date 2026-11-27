---
title: "FALCA: Falsification-Aware Reinforcement Learning with Hierarchical Credit Assignment for Long-Horizon Deep Search Agents"
authors: ["Zijun Dou", "Kun Luo", "Chaofan Li", "Shuqi Lu", "Zheng Liu"]
date: 2026-10-20
arxiv_id: "2610.28361v1"
url: "https://arxiv.org/abs/2610.28361"
score: 0.8
topics: [agentic RL, LLM agent, RL training, agentic]
status: unread
---

# FALCA: Falsification-Aware Reinforcement Learning with Hierarchical Credit Assignment for Long-Horizon Deep Search Agents

## Summary

FALCA frames long-horizon deep search as a propose-falsify loop: a Searcher proposes candidate answers while independent Falsifiers actively seek counterevidence, check unmet constraints, and produce revision reports to prevent early-error amplification. Training combines SFT warmup on falsification trajectories with agentic RL using parallel rollouts and hierarchical credit assignment across research stages, state transitions, and individual actions. Improves deep search performance on five benchmarks over backbone and harness ablations while measurably reducing confirmation bias and error accumulation.

## Key Contributions

- Collaborative Searcher-Falsifier architecture: independent falsifiers generate counterevidence reports rather than scoring existing answers
- Hierarchical credit assignment: three-level credit (research stage, state transition, action) addresses long-horizon credit sparsity
- SFT warmup on falsification trajectories before agentic RL stabilizes early training
- Explicit confirmation-bias reduction measured as an independent evaluation axis

## Relevance

Extends the long-horizon agentic RL thread (RLVB, PROVE) with a structural solution to error accumulation — where RLVB addresses commitment timing and PROVE addresses verification collusion, FALCA addresses confirmation bias via architectural separation of proposer and falsifier. The hierarchical credit assignment is a direct response to the credit sparsity problem in long-horizon search that PROVE also identified.

## My Thoughts

<!-- Add your own notes here -->
