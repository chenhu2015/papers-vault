---
title: "AutoScaffold: AI-Guided Scaffolding for Reinforcement Learning of Language Models"
authors: ["Zijian Zhang", "Rizhen Hu", "Jiangweizhi Peng", "Shiyang Li", "Sujay Bhatt", "Sihan Zeng", "Mingyi Hong"]
date: 2026-11-12
arxiv_id: "2611.14515v1"
url: "https://arxiv.org/abs/2611.14515"
score: 0.82
topics: [agentic RL, RL training, GRPO, LLM agent, tool use]
status: unread
---

# AutoScaffold: AI-Guided Scaffolding for Reinforcement Learning of Language Models

## Summary

AutoScaffold introduces a frozen teacher that periodically diagnoses student RLVR training trajectories and generates adaptive scaffolds — shared strategies across task classes and targeted hints for hard instances — without domain-specific intervention, removing scaffolds at evaluation. Applied identically to ALFWorld, search-based QA, math, and GPU kernel generation, students trained with AutoScaffold outperform RL baselines by 7.2 points (ALFWorld success) and 4.0 points (QA exact match). The teacher shifts scaffold content from step-by-step workflows to targeted fixes as the student improves, constituting a new teacher-student RLVR mechanism that bridges the agentic and reasoning domains.

## Key Contributions

- Unified AI-for-AI framework: frozen teacher observes student training experience and designs scaffolds in two forms — shared task-class strategies and per-instance hints — with no human design per domain
- Teacher adapts scaffold content and amount as student improves (step-by-step workflows early → targeted fixes late), confirmed through analysis
- Gains across four qualitatively different domains (ALFWorld, QA, math, GPU kernels) from one framework instance
- Surpasses QuestA on math using ~1/3 the student training steps via teacher-accelerated exploration

## Relevance

Extends the RAL/teacher-student RL thread: where RAL (Nov 11) used a co-trained LLM judge as sole reward, AutoScaffold uses a frozen teacher to generate adaptive guidance scaffolds — a complementary mechanism targeting the exploration bottleneck rather than the reward signal. The multi-domain applicability (agentic ALFWorld + reasoning math + systems GPU) makes it directly relevant to the agentic RL + tool use interests.

## My Thoughts

<!-- Add your own notes here -->
