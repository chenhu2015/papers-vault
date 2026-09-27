---
title: "HiDiffTIR: Hierarchical Difficulty-Aware Policy Optimization for Multi-Turn Tool-Integrated Reasoning"
authors: ["Yucan Guo", "Xiaohan Wang", "Miao Su", "Saiping Guan", "Zhongni Hou", "Jiajun Chai", "Wei Lin", "Guojun Yin", "Xiaolong Jin", "Jiafeng Guo", "Xueqi Cheng"]
date: 2026-08-22
arxiv_id: "2608.21863v2"
url: "http://arxiv.org/abs/2608.21863v2"
score: 0.82
topics: [agentic RL, tool use, RL training, LLM agent, GRPO]
status: unread
---

# HiDiffTIR: Hierarchical Difficulty-Aware Policy Optimization for Multi-Turn Tool-Integrated Reasoning

## Summary

HiDiffTIR addresses uniform credit assignment in tool-integrated reasoning (TIR) RL by performing difficulty-aware credit at both trajectory and turn levels, focusing policy updates on more informative trajectories and harder tool-use steps. The difficulty signal is derived purely from group-level statistics from standard RL rollouts — no additional supervision, reward model, or process annotations required. Three tool-using benchmarks show consistent improvement over strong RL baselines in both multi-turn TIR performance and tool invocation accuracy.

## Key Contributions

- Trajectory-level difficulty weighting: harder trajectories receive higher weight in policy gradient, de-emphasizing trivial samples
- Turn-level difficulty weighting: harder tool-invocation steps get higher weight within a trajectory
- Both difficulty signals derived from group statistics only — no extra data collection or annotation
- Evaluation specifically on tool invocation accuracy (not just final task success) — more granular than most TIR papers

## Relevance

Connects to the tool-use RL thread (Spurious Tool Use, EAPO, EvoCUA-1.5, Le Critique, MATCH). Where those papers focus on reward design for tool necessity/quality, HiDiffTIR focuses on *which* tool-use steps to emphasize during training. The difficulty-aware framing is also a lightweight alternative to DATPO's tree-based difficulty adaptation.

## My Thoughts

<!-- Add your own notes here -->
