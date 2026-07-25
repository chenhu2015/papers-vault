---
title: "TRACE: Turn-level Reward Assignment via Credit Estimation for Long-Horizon Agents"
authors: ["Leitian Tao", "Baolin Peng", "Wenlin Yao", "Tao Ge", "Hao Cheng", "Mike Hang Wang", "Jianfeng Gao", "Sharon Li"]
date: 2026-07-15
arxiv_id: "2607.13988v1"
url: "http://arxiv.org/abs/2607.13988v1"
score: 0.91
topics: [agentic RL, RL training, reward model, LLM agent, tool use]
status: unread
---

# TRACE: Turn-level Reward Assignment via Credit Estimation for Long-Horizon Agents

## Summary

TRACE assigns turn-level rewards to long-horizon agents by treating the log-probability of the gold answer under a frozen reference model as a state-value proxy, then computing per-action rewards as TD changes in that log-ratio value at tool-call boundaries. No critic or process-label training is required, and the one-step TD component telescopes across redundant tool calls. On BrowseComp-Plus (closed-web search), TRACE lifts Qwen3-4B from 7.2 to 35.6 and Qwen3-30B-A3B from 8.4 to 42.6 using pure RL with no SFT cold-start, and the learned behavior transfers to open-web benchmarks.

## Key Contributions

- Log-ratio state value: gold-answer log-probability under frozen reference model as implicit state quality signal — no separate value network or process labels
- Per-action reward = TD delta at each tool-call boundary; one-step TD telescopes across redundant intermediate tool calls (eliminates noisy credit for "nothing happened" steps)
- Pure RL from scratch without SFT cold-start or agentic mid-training; earlier convergence and faster learning curves than baseline
- Open-web transfer: search behavior learned on closed-web BrowseComp-Plus generalizes to open-web benchmarks without additional training

## Relevance

Directly closes gap #8 (step↔turn junction in credit assignment). The prior landscape: GRPO assigns trajectory-level advantage uniformly to all tokens; TACO/EGRSD identify high-credit tokens via heuristics; OPPO provides Bayesian recursion for token↔trajectory; BDA adds turn-level counterfactual. TRACE provides the turn-level TD bridge via the simplest possible state value — the model's implicit belief about eventual success — requiring no auxiliary networks. The +28.4 point gain on Qwen3-4B on BrowseComp-Plus is among the largest single-paper gains in the vault, establishing that dense turn-level credit (not just sparse trajectory reward) is load-bearing for long-horizon search tasks.

## My Thoughts

<!-- Add your own notes here -->
