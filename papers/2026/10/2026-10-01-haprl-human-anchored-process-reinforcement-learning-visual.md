---
title: "HaPRL: Human-Anchored Process Reinforcement Learning for Visual Search Agent"
authors: ["Zhangquan Chen", "Yaoxin Niu", "Xiang An", "Mingze Sun", "Zhumei Wang", "Chih-Ting Liao", "Hongkun Cao", "Ruqi Huang"]
date: 2026-10-01
arxiv_id: "2609.37190v1"
url: "http://arxiv.org/abs/2609.37190v1"
score: 0.87
topics: [multimodal models, vision language models, agentic RL, RL training]
status: unread
---

# HaPRL: Human-Anchored Process Reinforcement Learning for Visual Search Agent

## Summary

HaPRL addresses the unsupervised search process in multi-turn visual question answering by anchoring RL training on 1K+ human-annotated search traces rather than outcome-only rewards. A judge scores each rollout with task-adaptive weights against distilled human search behavior, preventing faulty-route reinforcement where incorrect reasoning accidentally produces correct final answers. Early-stage process supervision yields 6.7x more improvement in subsequent outcome-based scaling, suggesting process rewards are disproportionately valuable early in training.

## Key Contributions

- Identifies "faulty route" problem in outcome-only RL: erroneous search paths that accidentally reach correct answers get reinforced, corrupting the search policy
- Annotation platform collecting 1K+ human-annotated visual search traces with fine-grained behavioral signals
- Task-adaptive weight judge that scores rollouts against distilled human search traces rather than outcome labels
- Empirical finding: early-stage process supervision yields 6.7x improvement multiplier for subsequent outcome-based RL scaling — process rewards best used early, not throughout training

## Relevance

Bridges the multimodal/VLM RL thread (on monthly check since August) with the process reward design thread (InfoFlow, TGPO). This is the first VLM-specific agentic RL paper with explicit process reward design to appear in recent digests, and its finding that process rewards multiply later outcome-based gains is directly relevant to the open question of when/how to use intermediate rewards in agentic RL training curricula.

## My Thoughts

<!-- Add your own notes here -->
