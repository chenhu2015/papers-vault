---
title: "SPEAR: Distilling Domain-Adaptive Reasoning Skeletons via Sequential Symbolic Alignment in Reinforcement Learning"
authors: ["Zhuochun Li", "Yuelyu Ji", "Yiming Zeng", "Daqing He"]
date: 2026-08-27
arxiv_id: "2608.26550"
url: "http://arxiv.org/abs/2608.26550v1"
score: 0.80
topics: [RL training, agentic RL, reward model, RLAIF]
status: unread
---

# SPEAR: Distilling Domain-Adaptive Reasoning Skeletons via Sequential Symbolic Alignment in Reinforcement Learning

## Summary

SPEAR resolves the dilemma between sparse outcome rewards and expensive neural PRMs in RL-based knowledge distillation by projecting reasoning traces into domain-adaptive symbolic milestones and using LCS alignment to measure student-teacher process agreement. The resulting dense, order-aware reward signal enforces logical consistency during on-policy distillation without any external neural verifier, validated across math, science, and commonsense reasoning tasks.

## Key Contributions

- Projects natural-language reasoning traces into domain-adaptive symbolic milestones (skeleton extraction from teacher traces)
- Longest Common Subsequence (LCS) alignment between student explorations and teacher milestones provides dense, order-aware process reward
- Training-free and plug-and-play: no external neural verifier required, works as a reward module on top of existing RL-KD pipelines
- Validated across three reasoning domains (math, science, commonsense), showing effective reasoning gap closure via sequence-level on-policy distillation

## Relevance

SPEAR adds a third position to the distillation+RL design space alongside AToD (Aug 29, annealing teacher signal over training) and OPDVR (Aug 30, ReLU-gated fusion of distillation and RL objectives): SPEAR uses symbolic intermediate rewards derived from teacher traces to guide RL without requiring a separately trained PRM. This is directly relevant to the OPD origin-alignment thread from Sep 01 — SPEAR's symbolic skeleton is inherently domain-adaptive, which may explain how origin alignment operates: when teacher and student share the same symbolic milestone vocabulary, LCS alignment is meaningful; when they diverge, the skeleton becomes a poor proxy and transfer quality drops.

## My Thoughts

<!-- Add your own notes here -->
