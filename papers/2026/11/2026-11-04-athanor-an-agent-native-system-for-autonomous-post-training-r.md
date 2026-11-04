---
title: "Athanor: An Agent-Native System for Autonomous Post-Training Research"
authors: ["Yufa Zhou", "Yichen Wang", "Jiakun Fan", "Ziqi Shu", "Zhichao Liu", "Anru R. Zhang", "Neiwen Ling", "Zijun Wei"]
date: 2026-10-15
arxiv_id: "2610.21055v1"
url: "http://arxiv.org/abs/2610.21055v1"
score: 0.85
topics: [agentic RL, RL training, LLM agent, agentic, tool use]
status: unread
---

# Athanor: An Agent-Native System for Autonomous Post-Training Research

## Summary

Athanor is an open system where four Claude Opus 5.5 agents autonomously post-train a raw base model (Qwen3-4B-Base) in a 104-hour campaign, improving it from 15.9 to 67.3 on a development suite and from 9.2 to 48.2 on a held-out suite — matching the official Qwen3-4B-Instruct-2507 (66.5/47.9). Agents operate with full research autonomy: reading datasets, writing training algorithms, tuning hyperparameters, and iterating; they reach this level by recombining SFT, RL, weight merges, and self-distillation without external teacher models. This is the first demonstration that frontier agents can autonomously post-train a base model into a cross-domain generalist matching the official instruct version.

## Key Contributions

- Full-autonomy campaign: 4 agents × 8-GPU nodes, no research advice, 104 hours, sandbox with frozen evaluation and held-out suite
- Agents recombine known methods — SFT on public reasoning data, RL with rollout modification introduced by one agent, weight merges across agents, rounds of self-distillation — without discovering novel algorithms
- Athanor services provide frozen evaluation, managed jobs, decontaminated data, and persistent research record to constrain agent behavior and prevent benchmark contamination
- Key finding: today's agents already have engineering and research ability to conquer autonomous post-training; bottleneck is infrastructure, not reasoning

## Relevance

Directly advances the agentic RL thread: Athanor is the agentic RL system applied recursively — agents using RL and SFT to train better agents. Connects to RSI-Dojo (internalizing post-training) and CoHARL (co-evolving agent and harness) surfaced this week; the autonomous-research angle also connects to Sandman's sandbox infrastructure finding.

## My Thoughts

<!-- Add your own notes here -->
