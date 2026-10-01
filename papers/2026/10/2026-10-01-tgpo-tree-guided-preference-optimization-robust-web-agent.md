---
title: "TGPO: Tree-Guided Preference Optimization for Robust Web Agent Reinforcement Learning"
authors: ["Ziyuan Chen", "Zhenghui Zhao", "Zhangye Han", "Miancan Liu", "Xianhang Ye", "Yiqing Li", "Hongbo Min", "Jinkui Ren", "Xiantao Zhang", "Guitao Cao"]
date: 2026-10-01
arxiv_id: "2509.14172v2"
url: "http://arxiv.org/abs/2509.14172v2"
score: 0.79
topics: [agentic RL, RL training, reward model, LLM agent]
status: unread
---

# TGPO: Tree-Guided Preference Optimization for Robust Web Agent Reinforcement Learning

## Summary

TGPO proposes an offline RL framework for web agents that merges semantically identical states across trajectories into a tree-structured representation, eliminating label conflicts in preference learning. A Process Reward Model automatically generates fine-grained rewards through subgoal progress, redundancy detection, and action verification, while a dynamic weighting mechanism prioritizes high-impact decision points. Experiments on Online-Mind2Web and C-WebShop show higher success rates with fewer redundant steps compared to existing methods.

## Key Contributions

- Tree-structured trajectory representation: merges semantically identical states across multiple trajectories, converting the trajectory set into a DAG that removes contradictory preference labels at shared states
- Automatic PRM: generates fine-grained step rewards via subgoal progress scoring, redundancy detection, and action verification — no human annotation required
- Dynamic weighting: assigns higher learning weight to high-impact decision points in the trajectory tree
- Addresses credit assignment, annotation cost, and reward sparsity as a unified offline RL design

## Relevance

Complements ASCT and TGPO in the tree-credit cluster: where ASCT uses inference-time action trees for online credit assignment and TEMPO uses training-time prefix trees, TGPO uses an offline trajectory DAG with automatic PRM for web agents. The automatic PRM design (subgoal progress + redundancy + verification) is a concrete alternative to the cycle-consistency (CCS) and cross-attention self-supervised reward signals for generating step-level rewards without gold labels in agentic tasks.

## My Thoughts

<!-- Add your own notes here -->
