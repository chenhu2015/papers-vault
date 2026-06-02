---
title: "OpenWebRL: Demystifying Online Multi-turn Reinforcement Learning for Visual Web Agents"
authors: ["Rui Yang", "Qianhui Wu", "Yuxi Chen", "Hao Bai", "Wenlin Yao", "Hao Cheng", "Baolin Peng", "Huan Zhang", "Tong Zhang", "Jianfeng Gao"]
date: 2026-06-01
arxiv_id: "2606.02031v1"
url: "http://arxiv.org/abs/2606.02031v1"
score: 0.88
topics: [agentic RL, tool use, multimodal, VLM, LLM agent]
status: unread
---

# OpenWebRL: Demystifying Online Multi-turn Reinforcement Learning for Visual Web Agents

## Summary

OpenWebRL is an open end-to-end framework for training visual web agents with online multi-turn RL directly on live websites, covering scalable browser infrastructure, multimodal context management, and trajectory-level success judging. OpenWebRL-4B achieves 67.0% on Online-Mind2Web and 64.0% on DeepShop using only 0.4K initialization trajectories and 2.2K RL tasks, outperforming larger open-source agents and remaining competitive with proprietary systems. The paper also provides a systematic study of which design choices make online RL effective for visual web agents.

## Key Contributions

- Open framework (infrastructure, initialization, context management, reward judging) for multi-turn visual web agent RL on live websites
- OpenWebRL-4B achieves SOTA among open-source agents on Online-Mind2Web (67.0%) and DeepShop (64.0%) with minimal data
- Systematic ablation of key design choices (trajectory judging, context management, initialization strategy) that make online RL effective
- Release of training data, models, and code to support reproducibility

## Relevance

Long-horizon multi-turn agentic RL for visual agents was barely touched in recent digests; this directly extends the tool-use RL thread (EchoRL, DARTS, AdaptR1 — June 1) to the GUI/web domain with a full open-source training pipeline, resolving the open-source bottleneck for this setting.

## My Thoughts

<!-- Add your own notes here -->
