---
title: "ToolRLA: Multiplicative Reward Decomposition for Tool-Integrated Agents"
authors: ["Pengbo Liu"]
date: 2026-03-02
arxiv_id: "2603.01620v4"
url: "http://arxiv.org/abs/2603.01620v4"
score: 0.79
topics: [agentic RL, tool use, GRPO, RL training, LLM agent]
status: unread
---

# ToolRLA: Multiplicative Reward Decomposition for Tool-Integrated Agents

## Summary

ToolRLA proposes multiplicative reward decomposition for tool-using LLM agents: four dimensions (format validity, tool selection, parameter accuracy, compliance) are multiplied rather than added, encoding domain priority orderings as inductive biases so that a wrong tool selection cannot be compensated by correct parameters. A three-stage SFT→GRPO→DPO pipeline deploys this reward in a financial advisory copilot, achieving a 47% improvement in task completion, 63% reduction in tool invocation errors, and 93% reduction in regulatory violations over three months.

## Key Contributions

- **Multiplicative vs additive reward decomposition**: multiplication enforces strict priority ordering (format must pass before tool selection matters, etc.); ablations show +7pp improvement over additive alternatives
- **Four-dimensional reward**: format validity × tool selection × parameter accuracy × regulatory compliance; each dimension targets a distinct failure mode
- **Three-stage pipeline**: SFT cold-start → GRPO fine-tuning with multiplicative reward → DPO preference alignment for edge case refinement
- **Real-world deployment results**: 80+ advisors, 1,200+ daily queries, 3-month longitudinal evaluation — rare in LLM RL research

## Relevance

Extends the tool-use RL thread (EchoRL/DARTS/AdaptR1 — Jun 1, Training LLMs for Multi-Step Tool Orchestration — Jun 7) with a reward design insight: multiplicative decomposition matches the way tool-use correctness actually works (a wrong API call cannot be fixed by correct formatting). The SFT→GRPO→DPO pipeline complements the SIRI/ECPO discussion of what kind of signal each training stage provides.

## My Thoughts

<!-- Add your own notes here -->
