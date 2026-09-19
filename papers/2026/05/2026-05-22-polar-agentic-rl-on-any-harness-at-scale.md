---
title: "Polar: Agentic RL on Any Harness at Scale"
authors: ["Binfeng Xu", "Hao Zhang", "Shaokun Zhang", "Songyang Han", "Mingjie Liu", "Jian Hu", "Shizhe Diao", "Zhenghui Jin", "Yunheng Zou", "Michael Demoret", "Jan Kautz", "Yi Dong"]
date: 2026-05-22
arxiv_id: "2605.24220v1"
url: "http://arxiv.org/abs/2605.24220v1"
score: 0.87
topics: [agentic RL, tool use, LLM agent, GRPO]
status: unread
---

# Polar: Agentic RL on Any Harness at Scale

## Summary

Polar is a rollout framework that treats any agent harness as a black box for scalable asynchronous RL: it proxies LLM API calls, records token-level model interactions, and reconstructs token-faithful trajectories for GRPO training. Each rollout node independently handles execution, trajectory reconstruction, and evaluation in parallel, decoupled from the trainer to maximize compute utilization for long-running agent workloads. Validated on SWE-Bench Verified with multiple coding harnesses, Polar improves Qwen3.5-4B by 22.6 points with the Codex harness using simple GRPO.

## Key Contributions

- Black-box harness treatment: proxies LLM API calls to capture token-level interactions without modifying harness internals
- Token-faithful trajectory reconstruction: reconstructs training trajectories from API-level records, preserving full token detail for GRPO
- Decoupled asynchronous architecture: rollout nodes (execution + reconstruction + evaluation) run independently from trainer, scaling to long-running workloads
- Multi-harness validation: +22.6 / +4.8 / +0.6 / +6.2 on SWE-Bench Verified with Codex / Claude Code / Qwen Code / Pi harnesses

## Relevance

Polar is the practical counterpart to Harness-RL's CAPO: both treat the harness as a black box and address the engineering challenge of applying GRPO across heterogeneous agent execution environments. Polar's API-proxy approach differs from Harness-RL's prefix-tree gradient routing — comparing the two training signal designs is an open empirical question surfaced by this pair.

## My Thoughts

<!-- Add your own notes here -->
