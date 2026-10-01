---
title: "SIPO: Selective-Inference Policy Optimization for Tree-Structured Agentic RL"
authors: ["Zenghuang Fu", "Ningqi Chen", "Mingda Jia", "Xiaofeng Han", "Zhaoyang Li", "Qiuyuan Ai", "Zelong Zheng", "Haoyu Wu", "Tianyu Fu", "Chenxu Zhao", "Minghui Wu", "Guannan He", "Changwei Wang"]
date: 2026-10-01
arxiv_id: "2609.34805v1"
url: "http://arxiv.org/abs/2609.34805v1"
score: 0.93
topics: [agentic RL, RL training, GRPO, reward model]
status: unread
---

# SIPO: Selective-Inference Policy Optimization for Tree-Structured Agentic RL

## Summary

SIPO identifies a statistical asymmetry in tree-structured agentic RL: incumbent nodes are selected based on their own generation statistics, so branch values conflate selection history with continuation quality. It introduces three mechanisms — a scale-free branch criterion, exchangeable branching (fresh continuations from each selected parent), and order-statistic correction (adjusting incumbents by selection rank) — that preserve the leaf budget while removing the selection bias. On seven QA benchmarks with Qwen3-4B, Qwen3-8B, and Qwen2.5-7B, SIPO achieves the highest reported multi-hop and single-hop averages among compared methods.

## Key Contributions

- Formalises the selection-history asymmetry in tree-structured RL: incumbents selected by their own score → inflated branch value estimates that don't reflect pure continuation quality
- Scale-free branch criterion: normalises generation scores and sibling penalties to a consistent relative scale across the tree
- Exchangeable branching: samples multiple fresh continuations from each selected parent, providing an unbiased sibling reference
- Order-statistic correction: adjusts retained incumbent values using selection rank and the estimated score–outcome association, recovering an unbiased branch estimate without discarding incumbents

## Relevance

Directly answers the open question from the 2026-09-30 digest: TEMPO's prefix value might degrade due to selection history bias when branch statistics reflect which node was chosen rather than how well continuations proceed. SIPO provides the statistical mechanism to correct this, completing the TEMPO/ASCT/SIPO cluster as three complementary perspectives on tree-based credit in agentic RL.

## My Thoughts

<!-- Add your own notes here -->
