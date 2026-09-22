---
title: "ECHO: Prune To Act, Trace To Learn With Selective Turn Memory In Agentic RL"
authors: ["Zijun Xie", "Binbin Zheng", "Enlei Gong", "Jihua Liu", "Yuyang You", "Lingfeng Liu", "Jiayao Tang", "Guanqun Zhao", "Aoqi Hu", "Zeyu Chen"]
date: 2026-06-30
arxiv_id: "2606.31650v5"
url: "https://arxiv.org/abs/2606.31650"
score: 0.76
topics: [agentic RL, RL training, LLM agent, multi-turn]
status: unread
---

# ECHO: Prune To Act, Trace To Learn With Selective Turn Memory In Agentic RL

## Summary

ECHO resolves the mismatch between bounded-context acting and outcome-based RL by compressing each environment turn into a source-indexed memory record and routing positive outcome credit to reused evidence turns and memory-selection actions — not just the final segment. On BrowseComp-Plus, ECHO reaches 43.4% accuracy versus 28.9% GRPO and 36.1% rolling-summary SUPO while using fewer turns. Zero-shot generalization improves across multi-objective QA, code generation, and deep information-seeking on both dense and MoE backbones.

## Key Contributions

- Source-indexed memory records: each environment turn compressed into a compact record preserving provenance, enabling reconstruction of bounded policy contexts by record selection
- Credit routing: positive outcome credit propagated to the final trajectory segment, reused evidence turns, memory findings, and memory-selection actions — all via source indices
- Identifies and resolves the acting/learning mismatch: existing context compression methods lose provenance needed to assign credit to evidence that mattered
- State-of-the-art on BrowseComp-Plus with fewer turns than rolling-summary baseline (SUPO)

## Relevance

Directly extends the BATON inter-trajectory credit thread by operating at the intra-trajectory memory level: BATON / GRSD ask how to weight trajectories relative to each other, ECHO asks which turns within a trajectory earned the positive outcome. Together they address credit assignment at three granularities: turn (ECHO) → trajectory (BATON/GRSD) → group (ArenaFlow). The Dependency-Aware DAG (which prunes non-load-bearing rounds at structural level) is now complemented by ECHO's content-level provenance approach.

## My Thoughts

<!-- Add your own notes here -->
