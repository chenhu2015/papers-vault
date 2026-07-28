---
title: "MemAgent: Reshaping Long-Context LLM with Multi-Conv RL-based Memory Agent"
authors: ["Hongli Yu", "Tinghong Chen", "Jiangtao Feng", "Jiangjie Chen", "Weinan Dai", "Qiying Yu", "Ya-Qin Zhang", "Wei-Ying Ma", "Jingjing Liu", "Mingxuan Wang", "Hao Zhou"]
date: 2026-07-28
arxiv_id: "2507.02259"
url: "https://arxiv.org/abs/2507.02259"
score: 0.79
topics: [agentic RL, LLM agent, RL training, GRPO]
status: unread
---

# MemAgent: Reshaping Long-Context LLM with Multi-Conv RL-based Memory Agent

## Summary

Introduces MemAgent, an RL-trained agent workflow that reads long documents in segments and maintains a compact memory via an overwrite strategy, extending the DAPO algorithm to multi-conversation generation for end-to-end optimization without position extrapolation techniques. Trained on 8K context, MemAgent extrapolates to 3.5M-token QA tasks with less than 5% performance loss and achieves 95%+ accuracy on the 512K RULER test, demonstrating linear-complexity handling of effectively unbounded documents.

## Key Contributions

- Segment-based reading with overwrite memory strategy: agent reads in chunks and writes/updates a compressed memory rather than appending raw context
- Multi-Conv RL training: extends DAPO to independent-context multi-conversation generation, enabling RL training over segmented document processing
- Extreme context extrapolation: 8K training → 3.5M test context with <5% degradation, entirely without length extrapolation techniques
- 95%+ on 512K RULER, establishing a new paradigm for handling infinite-length documents via RL-trained memory management

## Relevance

Directly complements CompactionRL (Jul 26) in the in-loop memory management thread: CompactionRL jointly optimizes task execution and context compaction (summarization of prior trajectory) using cross-trajectory GAE; MemAgent instead trains a dedicated segment-reading + overwrite memory agent using DAPO, achieving infinite-length extrapolation without explicit trajectory compaction — a different architectural answer to the same problem of finite context windows in long-horizon agentic RL.

## My Thoughts

<!-- Add your own notes here -->
