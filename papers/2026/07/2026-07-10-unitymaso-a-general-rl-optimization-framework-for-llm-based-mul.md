---
title: "UnityMAS-O: A General RL Optimization Framework for LLM-Based Multi-Agent Systems"
authors: ["Yiqun Chen", "Wei Yang", "Erhan Zhang", "Shijie Wang", "Qi Liu", "Zechun Niu", "Bin Zhang", "Haitao Li", "Rui Li", "Lingyong Yan", "Jinyuan Feng", "Biqing Qi", "Xiaochi Wei", "Yan Gao", "Yi Wu", "Yao Hu", "Jiaxin Mao"]
date: 2026-07-10
arxiv_id: "2605.26646v1"
url: "https://arxiv.org/abs/2605.26646"
score: 0.75
topics: [agentic RL, LLM agent, RL training, tool use, RLHF]
status: unread
---

# UnityMAS-O: A General RL Optimization Framework for LLM-Based Multi-Agent Systems

## Summary

UnityMAS-O provides a unified RL optimization interface for LLM-based multi-agent workflows by treating the complete workflow (not a single policy) as the optimization unit, with first-class objects for logical agent roles, graph trajectories, user-defined rewards, and agent-model mappings that support full/partial/no parameter sharing. Backed by a Ray star-topology runtime extending veRL, it instantiates on retrieval-augmented QA, iterative agentic search, and reflective code generation, showing multi-agent RL improves over manually orchestrated workflows—especially for smaller models and strict all-passed code metrics. This is the most general LLM multi-agent RL substrate yet, analogous to TRIAGE/CRAFT/TAPO but operating at the workflow level rather than the trajectory level.

## Key Contributions

- Workflow-as-optimization-unit: complete agent workflow (not single trajectory) is the RL target; decouples logical agent roles from physical model parameters
- Role-specific credit assignment at three granularities: role level, turn level, trajectory level
- Flexible parameter sharing: full sharing, full separation, or partial sharing across agents
- Ray star-topology runtime extending veRL; instantiated on RAG-QA, agentic search, code generation tasks

## Relevance

UnityMAS-O addresses the multi-agent credit assignment problem at the workflow level, complementing the token- and step-level credit assignment thread (MRPO, GRPO-λ, EGSPO, TAPO, TRIAGE, CRAFT). Together with ARTIST (outcome-based multi-turn tool RL) and DynaWeb (model-based web agent RL), the vault now has a three-layer view of agentic RL infrastructure: DynaWeb handles environment simulation, ARTIST handles single-agent multi-turn tool learning, and UnityMAS-O handles multi-agent workflow optimization.

## My Thoughts

<!-- Add your own notes here -->
