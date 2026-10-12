---
title: "SOAR: Source-Aware Reinforcement Learning with Precise Credit Assignment for Search Agents"
authors: ["Shengze Huang", "Zihao Tang", "Jinluan Yang", "Xin Yu", "Zhenghao Lin", "Xiao Liu", "Zengxuan Wen", "Yeyun Gong", "Haizhen Huang", "Weiwei Deng", "Feng Sun", "Qi Zhang", "Fei Wu", "Kun Kuang"]
date: 2026-10-09
arxiv_id: "2610.13157v1"
url: "http://arxiv.org/abs/2610.13157v1"
score: 0.82
topics: [agentic RL, RL training, LLM agent, tool use]
status: unread
---

# SOAR: Source-Aware Reinforcement Learning with Precise Credit Assignment for Search Agents

## Summary

SOAR addresses evidence fabrication in RL-trained search agents by making information-source attribution explicit — disentangling external search evidence and internal knowledge into parallel observable streams via a Source-Aware Workflow. A Source-Consistent Reward then guides policy evolution by assigning credit differentially by source, reducing fabrication by 74.8% while improving accuracy by 5–7 pp on 3B and 7B models. Rather than assigning credit to retrieval steps post-hoc, SOAR restructures the reasoning trajectory itself so that source attribution is a first-class object during RL training.

## Key Contributions

- Source-Aware Workflow: disentangles external (search) vs. internal (parametric) evidence into parallel, observable streams during reasoning
- Source-Consistent Reward: credit assignment conditioned on source attribution rather than just answer correctness
- 74.8% reduction in evidence fabrication — agents trained with SOAR are less likely to bypass external search results
- 5–7 pp accuracy gain on knowledge-intensive benchmarks across 3B and 7B model sizes

## Relevance

Directly extends the "Beyond Outcome Rewards" tool-call credit thread (now retired from targeted follow-up) in an unexpected direction: SOAR doesn't add post-hoc step rewards but instead restructures the trajectory format to expose source attribution as a structural object that reward can attach to. This is a qualitatively different approach to retrieval credit assignment and connects to the GACA / SHARPO cluster's ideas about multi-source advantage decomposition.

## My Thoughts

<!-- Add your own notes here -->
