---
title: "OpenForgeRL: Train Harness-native Agents in Any Environment"
authors: ["Xiao Yu", "Baolin Peng", "Ruize Xu", "Hao Zou", "Qianhui Wu", "Hao Cheng", "Wenlin Yao", "Nikhil Singh", "Zhou Yu", "Jianfeng Gao"]
date: 2026-07-24
arxiv_id: "2607.21557"
url: "http://arxiv.org/abs/2607.21557v1"
score: 0.88
topics: [agentic RL, tool use, LLM agent, RL training]
status: unread
---

# OpenForgeRL: Train Harness-native Agents in Any Environment

## Summary

OpenForgeRL solves the problem of training harness-native LLM agents (e.g., Claude Code, Codex) end-to-end by introducing a lightweight proxy that intercepts harness model calls and records them as standard RL training data, paired with a Kubernetes orchestrator that isolates each rollout in a remote container. This decoupled training-inference architecture enables any RL codebase (e.g., veRL) to train agents running real harnesses in any environment at scale. OpenForgeClaw achieves 31.7 pass³ on ClawEval; OpenForgeGUI reaches 63.0 on Online-Mind2Web and 72.3 on WebVoyager, matching or surpassing models several times larger in GUI settings.

## Key Contributions

- Lightweight harness proxy: intercepts model calls from any harness (Claude Code, Codex, OpenClaw, ZeroClaw) and records them as training trajectories for standard RL stacks
- Kubernetes-based rollout orchestrator: each rollout runs in an isolated remote container, enabling scale without shared state or environment contamination
- Empirical finding that harness choice significantly affects RL trainability — some harnesses are substantially harder for agents to learn with than others
- RL improves agentic reliability (self-verification, tool coverage, multi-step plan completion) but critical abilities like error recovery remain weak even after training

## Relevance

This directly extends the agentic RL and tool use threads: it provides the first open framework for training agents inside real inference harnesses (including Claude Code), making the rollout topology insights from BPO and the environment diversity insights from ToolVerse implementable at production scale. The finding that harness choice affects RL trainability is a new structural variable not yet characterized in the vault's agentic RL literature.

## My Thoughts

<!-- Add your own notes here -->
