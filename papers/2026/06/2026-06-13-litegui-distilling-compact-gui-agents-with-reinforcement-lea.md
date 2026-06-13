---
title: "LiteGUI: Distilling Compact GUI Agents with Reinforcement Learning"
authors: ["Yubin Wu", "Zicheng Cai", "Liping Ning", "Hua Wang", "Zhi Chen", "Yaohua Tang", "Hao Chen"]
date: 2026-06-13
arxiv_id: "2605.07505"
url: "https://arxiv.org/abs/2605.07505"
score: 0.82
topics: [agentic RL, GRPO, VLM, vision-language, LLM agent]
status: unread
---

# LiteGUI: Distilling Compact GUI Agents with Reinforcement Learning

## Summary

LiteGUI proposes a SFT-free training paradigm for small-scale (2B/3B) GUI agents: Guided On-Policy Distillation uses oracle reference trajectories with dynamic retrieval to reduce hallucination, followed by Multi-solution Dual-level GRPO that jointly aligns macro subtask planning with micro action execution. The core finding is that small GUI models fail from SFT-induced policy rigidity, not capacity limits — on-policy distillation plus multi-solution GRPO allows 2B/3B models to match substantially larger baselines.

## Key Contributions

- Guided On-Policy Distillation (GOD): oracle reference trajectories with dynamic retrieval reduce hallucination and cognitive misalignment in multi-solution GUI tasks
- Multi-solution Dual-level GRPO: macro-level (subtask planning) + micro-level (execution matching) joint alignment improves long-horizon GUI exploration
- Automated data pipeline synthesizing GUI trajectories with multi-solution annotations
- 2B/3B models match much larger baselines; SFT-free paradigm consistently outperforms conventional imitation learning across multiple GUI benchmarks

## Relevance

Extends the GRPO-for-agents thread into the GUI domain: where LiteGUI applies multi-solution GRPO at two action granularities (planning + execution), the earlier ToolRLA (Jun 12) applied multiplicative reward decomposition for tool-use priority — both are responses to the observation that single-level reward signals fail to capture the hierarchy of GUI/tool-use decisions.

## My Thoughts

<!-- Add your own notes here -->
