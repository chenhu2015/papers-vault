---
title: "Beyond Outcome Rewards: Constructing and Assigning Retrieval Credit for Search Agents"
authors: ["Wenyu Huang", "Xinyu Hou", "Pavlos Vougiouklis", "Ruofei Lai"]
date: 2026-10-08
arxiv_id: "2610.10179v1"
url: "http://arxiv.org/abs/2610.10179v1"
score: 0.91
topics: [agentic RL, reward model, RL training, LLM agent, tool use]
status: unread
---

# Beyond Outcome Rewards: Constructing and Assigning Retrieval Credit for Search Agents

## Summary

This paper systematically investigates intermediate supervision for training search agents with RLVR, comparing reward-shaping and credit-assignment strategies that provide learning signals from intermediate retrieval steps rather than only from final outcomes. The authors show that both the choice of intermediate signal and where its credit is assigned materially affect training behavior, and propose a training framework combining intermediate retrieval step signals with final outcome rewards. Experiments across multiple benchmarks demonstrate aggregate improvements in search-agent performance under matched training conditions.

## Key Contributions

- Systematic comparison of reward-shaping vs. credit-assignment strategies for intermediate retrieval supervision in RLVR
- Training framework combining intermediate retrieval step signals with sparse final outcome rewards
- Empirical finding that signal choice and credit assignment location are both independent design dimensions with significant impact
- Benchmark suite comparing search-agent RLVR under matched training conditions

## Relevance

Extends the step-credit cluster to retrieval/search agents: retrieval steps are a new domain where the question of "which intermediate action deserves credit" is live and underexplored. Directly adjacent to NTEP-R (tool-call credit for agentic VLMs) but applied to text-based search agents, generalizing the credit-assignment thread to information-retrieval tool use.

## My Thoughts

<!-- Add your own notes here -->
