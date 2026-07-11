---
title: "TSR: Trajectory-Search Rollouts for Multi-Turn RL of LLM Agents"
authors: ["Aladin Djuhera", "Swanand Ravindra Kadhe", "Farhan Ahmed", "Syed Zawad", "Heiko Ludwig", "Holger Boche"]
date: 2026-07-11
arxiv_id: "2602.11767"
url: "https://arxiv.org/abs/2602.11767"
score: 0.84
topics: [agentic RL, RL training, GRPO, LLM agent, tool use]
status: unread
---

# TSR: Trajectory-Search Rollouts for Multi-Turn RL of LLM Agents

## Summary

TSR embeds tree-style search (best-of-N, beam search, shallow lookahead) into the rollout generation phase of multi-turn RL training rather than at inference time, selecting high-scoring actions at each turn via state-based feedback to build higher-quality training trajectories. The approach is optimizer-agnostic and compatible with both PPO and GRPO, adding a one-time compute cost during training without modifying the inference pipeline. Achieves up to 15% performance gains on agentic benchmarks including Sokoban, FrozenLake, and WebShop.

## Key Contributions

- Reframes test-time search (MCTS, beam search) as a training-time rollout quality mechanism, introducing TSR as a modular add-on to existing policy gradient optimizers
- Three instantiations: best-of-N selection, beam search at each turn, and shallow lookahead — all use state-based feedback to score and select actions during rollout construction
- Demonstrates optimizer-agnosticism: TSR improves both PPO and GRPO without algorithm-specific modification
- Provides a complementary mechanism to rejection sampling: TSR constructs better trajectories during rollout rather than filtering after the fact

## Relevance

This paper directly answers the Jul 10 queue thread on MCTS-based RLVR extensions — it is the training-time analog of ROSE's search-time semantic-entropy branching. Where ROSE branches on semantic entropy to explore diverse *reasoning paths* for a fixed problem, TSR branches on state-based scores to explore diverse *action sequences* across multi-turn agentic tasks. Together they cover two granularities of tree-based quality improvement: within-reasoning (ROSE) and across-turns (TSR).

## My Thoughts

<!-- Add your own notes here -->
