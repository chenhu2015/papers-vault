---
title: "EnvFactory: Scaling Tool-Use Agents via Executable Environments Synthesis and Robust RL"
authors: ["Minrui Xu", "Zilin Wang", "Mengyi DENG", "Zhiwei Li", "Zhicheng Yang", "Xiao Zhu", "Yinhong Liu", "Boyu Zhu", "Baiyu Huang", "Chao Chen", "Heyuan Deng", "Fei Mi", "Lifeng Shang", "Xingshan Zeng", "Zhijiang Guo"]
date: 2026-08-08
arxiv_id: "2605.18703v1"
url: "http://arxiv.org/abs/2605.18703v1"
score: 0.73
topics: [agentic RL, tool use, LLM agent]
status: unread
---

# EnvFactory: Scaling Tool-Use Agents via Executable Environments Synthesis and Robust RL

## Summary

EnvFactory automates the construction of stateful executable tool environments for agentic RL by autonomously exploring and verifying real-world API resources, then synthesizing multi-turn trajectories with implicit human intents via topology-aware sampling and calibrated refinement. Using only 85 verified environments across 7 domains it generates 2,575 SFT and RL training trajectories, achieving +15% on BFCLv3 and +8.6% on MCP-Atlas with Qwen3-series models despite using 5× fewer environments than prior work.

## Key Contributions

- Autonomous environment discovery and verification from real-world API resources (no pre-collected documents)
- Topology-aware trajectory synthesis with calibrated refinement to produce natural multi-turn queries with implicit intents
- Efficient scaling: 85 environments → 2,575 SFT+RL trajectories, outperforming 5× larger environment sets
- Strong gains on tool-use benchmarks: +15% on BFCLv3, +8.6% on MCP-Atlas, improvements on τ²-Bench and VitaBench

## Relevance

EnvFactory addresses the environment construction bottleneck in agentic RL from the infrastructure side — complementary to EnvACE (Aug 8), which eliminates the external environment entirely via world rehearsal. Together, these two Aug 8 papers represent polar approaches to the same bottleneck: EnvFactory scales real environment construction through automation; EnvACE removes the requirement for real environments by internalizing dynamics. The topology-aware sampling and implicit intent calibration are notable — they address the "over-specified trajectory" problem (synthetic trajectories resembling instruction sequences rather than natural queries) that limits RL training effectiveness.

## My Thoughts

<!-- Add your own notes here -->
