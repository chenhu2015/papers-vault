---
title: "SENTINEL: Failure-Driven Reinforcement Learning for Training Tool-Using Language Model Agents"
authors: ["Ziyi Wang", "Yuxuan Lu", "Yimeng Zhang", "Qun Liu", "Chen Luo", "Jiri Gesi", "Hanqing Lu", "Yisi Sang", "Manling Li", "Jing Huang", "Dakuo Wang"]
date: 2026-06-11
arxiv_id: "2606.12908v1"
url: "http://arxiv.org/abs/2606.12908v1"
score: 0.84
topics: [agentic RL, RL training, tool use, LLM agent]
status: unread
---

# SENTINEL: Failure-Driven Reinforcement Learning for Training Tool-Using Language Model Agents

## Summary

SENTINEL addresses the task-distribution mismatch problem in agentic RL training: as the policy improves, a fixed task set becomes increasingly uninformative. A Controller-Proposer-Solver loop continuously analyzes rollout failures, synthesizes new tasks that stress the observed weaknesses, and trains the Solver on those targeted tasks. On Tau2-Bench Retail with Qwen3-4B-Thinking, SENTINEL improves Pass^1 from 66.4 to 74.9, outperforming RL on general synthetic tasks across all Pass^k metrics.

## Key Contributions

- **Controller-Proposer-Solver loop**: Controller identifies recurring error patterns in failed trajectories, Proposer generates executable tasks targeting those patterns, Solver trains on them
- **Failure-driven curriculum**: rollout failures are a scalable and targeted source of training signal, avoiding the static distribution mismatch of fixed task sets
- **Strong empirical results**: Pass^1 66.4→74.9 on Tau2-Bench Retail; outperforms RL with general synthetic tasks on all Pass^k metrics
- **Scalable signal extraction**: the framework converts every failure into training signal without requiring human annotation or manual task design

## Relevance

Directly extends the agentic RL curriculum thread (SUPERNOVA, Search Agent Training Study) by addressing the dynamic task distribution problem: instead of curating a fixed training set, SENTINEL makes the training distribution adaptive to current policy weaknesses. The Controller→Proposer→Solver decomposition is a clean agentic meta-RL framework that complements SIRI's (Jun 8) skill internalization approach.

## My Thoughts

<!-- Add your own notes here -->
