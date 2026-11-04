---
title: "Training LLM Agents to Automate LLM Post-Training with RSI-Dojo"
authors: ["Shuzheng Gao", "Zhaojian Yu", "Penghao Yin", "Yuling Shi", "Kai Cai", "Shilin He", "Michael R. Lyu"]
date: 2026-10-29
arxiv_id: "2611.03698v1"
url: "http://arxiv.org/abs/2611.03698v1"
score: 0.82
topics: [agentic RL, RL training, LLM agent, agentic, RLHF]
status: unread
---

# Training LLM Agents to Automate LLM Post-Training with RSI-Dojo

## Summary

RSI-Dojo addresses recursive self-improvement by internalizing the ability to conduct LLM post-training into the model itself, rather than outsourcing to workflow-level orchestration. RSI-Craft automatically converts research papers into 281 executable model training tasks with datasets, metrics, and evaluation dependencies. Fine-tuning Qwen3.5-9B/35B on collected trajectories yields RSI-Dojo-9B and RSI-Dojo-35B-A3B, improving over base models by 8.74 and 16.87 PostTrainBench points respectively, with RSI-Dojo-35B-A3B matching frontier models GLM-5.2 and GPT-5.5 on PostTrainBench.

## Key Contributions

- RSI-Craft: automatic pipeline that converts research papers (from top venues) into executable model training environments with unified dataset/metric interface
- RSI-Dojo: 281 seed training tasks filtered by data size, execution reliability, and discriminability
- Trajectory collection from frontier models with rubric-based and outcome-based filtering
- Demonstrates that the gap between workflow-level and model-internalized post-training automation is bridgeable with supervised fine-tuning on high-quality trajectories

## Relevance

Complements Athanor (also surfaced today) on the autonomous post-training research thread: Athanor shows frontier agents can autonomously run campaigns; RSI-Dojo shows how to teach smaller models to do the same by internalizing the skill. The RSI framing directly connects to the long-horizon agentic RL thread's interest in self-improving systems.

## My Thoughts

<!-- Add your own notes here -->
