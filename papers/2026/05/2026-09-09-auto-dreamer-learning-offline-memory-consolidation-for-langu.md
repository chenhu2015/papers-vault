---
title: "Auto-Dreamer: Learning Offline Memory Consolidation for Language Agents"
authors: ["Chongrui Ye", "Yuxiang Liu", "Yu Wang", "Haofei Yu", "Yining Zhao", "Ge Liu", "Julian McAuley", "Jiaxuan You"]
date: 2026-09-09
arxiv_id: "2605.20616v1"
url: "http://arxiv.org/abs/2605.20616v1"
score: 0.83
topics: [agentic RL, GRPO, LLM agent, tool use]
status: unread
---

# Auto-Dreamer: Learning Offline Memory Consolidation for Language Agents

## Summary

Auto-Dreamer trains a learned offline memory consolidator for language agents via GRPO, decoupling fast per-session memory acquisition from slow cross-session consolidation. Given a region of a typed memory bank, the consolidator uses bounded tool-use to inspect entries and source trajectories, then synthesizes a compact replacement set that abstracts recurring patterns across sessions. Trained on ScienceWorld alone, it outperforms RL-trained baselines on ScienceWorld by 7 points using 12x less memory, and transfers zero-shot to ALFWorld and WebArena.

## Key Contributions

- Decouples per-session memory acquisition (fast, online) from cross-session consolidation (slow, offline) inspired by complementary learning systems theory
- The consolidator is treated as a tool-using agent trained end-to-end with GRPO using downstream agent performance as the reward signal
- Cross-session consolidation: reads a memory region as evidence, uses bounded tool calls to inspect provenance-linked source trajectories, and synthesizes a compact replacement set
- 12x memory reduction on ScienceWorld with +7 points over RL-trained baselines; zero-shot transfer to ALFWorld (6x less memory) and WebArena

## Relevance

Directly advances the "agentic RL" and "GRPO" threads dominant in recent digests — this is a novel application of GRPO to meta-learning over memory structure rather than task execution, orthogonal to the multi-turn credit assignment work (TRIAL, SAPO, T-STAR, SAO) found Sep 08. The offline consolidation angle is structurally similar to the Agentic-DPO offline preference thread identified as an open gap (SFT-free VLM RL), applied here to memory rather than policy.

## My Thoughts

<!-- Add your own notes here -->
