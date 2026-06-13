---
title: "CUA-Gym: Scaling Verifiable Training Environments and Tasks for Computer-Use Agents"
authors: ["Bowen Wang", "Dunjie Lu", "Junli Wang", "Tianyi Bai", "Shixuan Liu", "Zhipeng Zhang", "Haiquan Wang", "Hao Hu", "Tianbao Xie", "Shuai Bai", "Dayiheng Liu", "Que Shen", "Junyang Lin", "Tao Yu"]
date: 2026-06-13
arxiv_id: "2605.25624"
url: "https://arxiv.org/abs/2605.25624"
score: 0.85
topics: [agentic RL, tool use, LLM agent, reward model]
status: unread
---

# CUA-Gym: Scaling Verifiable Training Environments and Tasks for Computer-Use Agents

## Summary

CUA-Gym is a scalable RLVR pipeline for computer-use agents that co-generates task instructions, environment states, and reward functions via a Generator–Discriminator–Orchestrator agent loop, yielding 32,112 verified training tuples across 110 environments. Models trained with GSPO achieve 62.1%/72.6% on OSWorld-Verified at 3B/17B scale, with performance scaling smoothly in both data volume and environment diversity, and transfer to held-out WebArena.

## Key Contributions

- Co-generation loop: Generator builds initial/golden environment states, Discriminator writes reward functions, Orchestrator drives iterative refinement with LLM majority-vote final filter
- CUA-Gym-Hub: suite of synthetic mock web applications grounded in real-world software-use distributions, enabling broad environment diversity
- 32,112 verified RLVR training tuples across 110 environments — magnitude larger than prior hand-curated CUA benchmarks
- GSPO-trained 3B/17B models achieve 62.1%/72.6% on OSWorld-Verified; scaling holds in data volume and environment diversity; transfer to WebArena confirmed

## Relevance

This is the first large-scale RLVR dataset explicitly targeting computer-use agents, directly extending the verifiable-environment + agentic-RL thread (SENTINEL, RACES, ToolRLA) to GUI/desktop interaction. The Generator-Discriminator-Orchestrator co-generation architecture mirrors the SENTINEL controller–proposer–solver pattern adapted to environment synthesis rather than failure-driven task generation.

## My Thoughts

<!-- Add your own notes here -->
