---
title: "StructRL: Online Structured Reinforcement Learning for Long-Horizon Vision-Language-Action Tasks"
authors: ["Ziyi Yin", "Sangmin Woo", "Kang Zhou", "Sungyeon Kim", "Aosong Feng", "Haibo Ding", "Jun Huan"]
date: 2026-09-28
arxiv_id: "2609.36352v1"
url: "http://arxiv.org/abs/2609.36352v1"
score: 0.73
topics: [agentic RL, reinforcement learning, LLM agent, multimodal models]
status: unread
---

# StructRL: Online Structured Reinforcement Learning for Long-Horizon Vision-Language-Action Tasks

## Summary

StructRL addresses sparse terminal-only rewards in online RL for long-horizon VLA models (GR00T-N1.5, pi 0.5) by decomposing tasks into verifiable subtasks with prerequisite-gated intermediate rewards scaled by completion pace. The structured supervision design prevents rewarding early subtask completions before prerequisites are satisfied, giving denser and semantically meaningful credit across long manipulation trajectories on RoboCasa365 and LIBERO-Long. The prerequisite-gated intermediate reward structure is structurally related to compositional credit assignment approaches in the step-credit and agentic RL threads.

## Key Contributions

- Decomposition of long-horizon VLA tasks into verifiable subtasks with explicit prerequisite ordering
- Prerequisite-gated intermediate rewards: reward for subtask N only after subtask N-1 is verified complete
- Completion pace scaling: reward magnitude proportional to how quickly the subtask was achieved
- State-of-the-art results on RoboCasa365 and LIBERO-Long with GR00T-N1.5 and pi 0.5 over online RL baselines

## Relevance

Connects the agentic RL and step-credit threads in a robotics VLA setting: the prerequisite-gated intermediate reward is structurally analogous to Compositional RL's (Oct 16) Shapley-value multi-agent credit and StructRL's subtask decomposition echoes SPLIT-RL's phased training. Provides a concrete instantiation of structured intermediate supervision for long-horizon multimodal agents that could generalize beyond manipulation to LLM agents.

## My Thoughts

<!-- Add your own notes here -->
