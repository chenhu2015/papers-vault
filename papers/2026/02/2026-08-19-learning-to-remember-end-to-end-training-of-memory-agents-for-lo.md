---
title: "Learning to Remember: End-to-End Training of Memory Agents for Long-Context Reasoning"
authors: ["Kehao Zhang", "Shangtong Gui", "Sheng Yang", "Wei Chen", "Yang Feng"]
date: 2026-02-13
arxiv_id: "2602.18493v1"
url: "https://arxiv.org/abs/2602.18493"
score: 0.77
topics: [agentic RL, LLM agent, RL training]
status: unread
---

# Learning to Remember: End-to-End Training of Memory Agents for Long-Context Reasoning

## Summary

UMA unifies memory operations (create, update, delete, reorganize) and question-answering within a single reinforcement-learning policy, maintaining a dual representation of a compact core summary and a structured CRUD Memory Bank for proactive consolidation during streaming. Ledger-QA, a new diagnostic benchmark, tests continuous state tracking where answers derive from accumulated updates rather than local span retrieval. UMA substantially outperforms long-context and RAG baselines across 13 datasets on dynamic reasoning and learning tasks.

## Key Contributions

- Unified Memory Agent (UMA): single RL policy combining CRUD memory operations and QA, trained end-to-end
- Dual memory representation: compact core summary (global context) + structured CRUD Memory Bank (explicit key-value entries with proactive consolidation)
- Ledger-QA benchmark: continuous state tracking where correct answers require integrating accumulated updates, not local retrieval
- Outperforms long-context LLMs and RAG baselines on dynamic reasoning and learning tasks across 13 datasets

## Relevance

The Memory + RL training signal thread queued from Aug 18 specifically sought papers where memory content becomes a training signal or reward target for RL. UMA trains the memory management policy end-to-end via RL, making the quality of memory operations directly subject to reward — this is the RL-as-training-signal angle the Aug 18 digest identified as the richest unexplored direction in the memory space (distinct from storage/retrieval papers like MemAgent which use RL to drive a pre-defined memory workflow).

## My Thoughts

<!-- Add your own notes here -->
