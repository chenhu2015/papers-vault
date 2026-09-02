---
title: "WM-R1: Training GUI Agents to Reason and leverage World Models with Reinforcement Learning"
authors: ["Yu Han", "Tianwen Qian"]
date: 2026-08-27
arxiv_id: "2608.27508"
url: "http://arxiv.org/abs/2608.27508v1"
score: 0.76
topics: [agentic RL, RL training, VLM, LLM agent, multimodal]
status: unread
---

# WM-R1: Training GUI Agents to Reason and leverage World Models with Reinforcement Learning

## Summary

WM-R1 replaces real Android environment interactions with world-model state transitions during all RL rollouts for mobile GUI agents, enabling massively parallelized step-level trajectory generation. The world model is embedded into the agent's thinking process so it can reason about candidate action consequences before committing, with a multi-dimensional rule-based reward jointly optimizing task success, trajectory efficiency, and world model utilization.

## Key Contributions

- World model serves as state-transition oracle for all rollouts, eliminating real Android environment interaction during RL training
- World model embedded in thinking chain: agent reasons about action consequences before selecting the final action (world-model-grounded CoT)
- Multi-dimensional rule-based reward: task success + trajectory efficiency + world model utilization — verifiable without a separate reward model
- High-quality 2000-task training dataset, curated for challenge; outperforms GRPO-only baselines and inference-time simulation methods

## Relevance

WM-R1 extends the VLM agentic RL thread (VAGEN Aug 22 — world-model reasoning for multi-turn VLM agents) to the mobile GUI domain, but adds a novel twist: the world model is embedded inside the thinking process rather than being an external simulator. This connects to HARTS (today) which also targets the environment-interaction bottleneck in agentic RL, but from an algorithmic angle (world-model rollout) rather than a systems angle (prefix sharing). The multi-dimensional verifiable reward approach also parallels EDGE (Aug 22), which used environment execution feedback as a verifiable signal.

## My Thoughts

<!-- Add your own notes here -->
