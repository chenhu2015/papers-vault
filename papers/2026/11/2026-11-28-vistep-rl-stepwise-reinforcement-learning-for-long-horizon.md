---
title: "ViStep-RL: Stepwise Reinforcement Learning for Long-Horizon Visual Agents"
authors: ["Junyang Chen", "Yao Qin", "Xiao Li", "Ningchao Wang", "Yiguo Qiao"]
date: 2026-11-18
arxiv_id: "2611.24170"
url: "https://arxiv.org/abs/2611.24170"
score: 0.80
topics: [agentic RL, VLM, vision-language, multimodal, RL training, LLM agent]
status: unread
---

# ViStep-RL: Stepwise Reinforcement Learning for Long-Horizon Visual Agents

## Summary

ViStep-RL models long-horizon visual agent execution as a dependency-linked graph of evidence-bearing subgoals, where a verifier tracks which subgoals are supported by valid visual evidence. Changes in graph potential serve as a dense, stepwise reward signal that structures the final-answer reward into intermediate subgoal milestones, directly addressing the sparse-reward problem for long-horizon VLM agents. The dependency-graph formulation connects to the SGR-OPSD and FALCA threads on structured credit assignment, now applied to visual evidence chains.

## Key Contributions

- Models execution as a directed graph of evidence-bearing subgoals with explicit dependency edges
- Verifier tracks which subgoals are satisfied by current visual evidence at each step
- Graph-potential-change reward provides dense intermediate signal without requiring human-labelled step rewards
- Addresses the evidence retention problem: observations must remain usable as the task unfolds across many steps

## Relevance

Connects to the agentic credit assignment thread (SGR-OPSD used subgoal plans + empirical progress graph; FALCA used hierarchical credit for research stages); ViStep-RL adds a dependency-graph evidence verifier specifically for the visual modality. This is a direct multimodal extension of the subgoal-based credit assignment work, following the CARE thread on VLM-specific credit problems.

## My Thoughts

<!-- Add your own notes here -->
