---
title: "SOLAR-RL: Semi-Online Long-horizon Assignment Reinforcement Learning"
authors: ["Jichao Wang", "Liuyang Bian", "Yufeng Zhou", "Han Xiao", "Yue Pan", "Guozhi Wang", "Hao Wang", "Zhaoxiong Wang", "Yafei Wen", "Xiaoxin Chen", "Shuai Ren", "Lingfang Zeng"]
date: 2026-04-24
arxiv_id: "2604.22558"
url: "https://arxiv.org/abs/2604.22558"
score: 0.81
topics: [agentic RL, RL training, LLM agent, reward model]
status: unread
---

# SOLAR-RL: Semi-Online Long-horizon Assignment Reinforcement Learning

## Summary

SOLAR-RL bridges offline and online RL for long-horizon GUI agent training by reconstructing diverse rollout candidates from static data, detecting first failure points via per-step validity signals, and retroactively assigning dense step-level rewards that simulate online feedback without live interaction costs. The semi-online framework captures global trajectory semantics — task completion and execution quality — that pure offline RL systematically misses. It significantly improves long-horizon task completion rates on GUI navigation benchmarks over strong baselines.

## Key Contributions

- Semi-online RL framework: reconstructs rollout diversity from static offline data without expensive live environment interaction
- First-failure-point detection using per-step validity signals for precise credit assignment in long-horizon trajectories
- Retroactive dense step-level reward assignment with target-aligned shaping that reflects trajectory-level execution quality
- Substantial improvements in GUI navigation long-horizon task completion rates with sample efficiency gains

## Relevance

Directly addresses the credit assignment and long-horizon bottleneck in agentic RL training — a core challenge identified across multiple recent digests. The semi-online approach is a novel middle ground between offline preference learning (DPO/KTO) and expensive fully online RL that has been largely unexplored in prior digests.

## My Thoughts

<!-- Add your own notes here -->
