---
title: "Reinforcement Learning for LLM-based Multi-Agent Systems through Orchestration Traces"
authors: ["Chenchen Zhang"]
date: 2026-05-04
arxiv_id: "2605.02801v1"
url: "https://arxiv.org/abs/2605.02801v1"
score: 0.85
topics: [agentic RL, LLM agent, tool use, GRPO]
status: unread
---

# Reinforcement Learning for LLM-based Multi-Agent Systems through Orchestration Traces

## Summary

This paper introduces a taxonomy of RL for multi-agent LLM systems organised around orchestration traces—temporal interaction graphs capturing sub-agent spawning, delegation, communication, aggregation, and stopping decisions. It maps reward design (eight families including parallelism-speedup and aggregation-quality rewards), credit-bearing units (token to team), and five orchestration sub-decisions, identifying the stopping decision as a gap with no published explicit RL training method. The work connects academic methods to industrial deployments including Anthropic Claude Code and releases an 84-entry tagged paper pool with a JSON schema for replayable orchestration traces.

## Key Contributions

- Formal taxonomy of RL for multi-agent LLM systems via orchestration traces (temporal interaction graphs)
- Maps three axes: reward design (8 families), credit/signal-bearing units (token→team), five orchestration sub-decisions (spawn, delegate, communicate, aggregate, stop)
- Identifies stopping decision as an open RL training gap (no explicit method published as of May 4, 2026)
- Connects academic methods to industrial evidence from Kimi Agent Swarm, OpenAI Codex, and Anthropic Claude Code; releases 84-entry tagged paper pool

## Relevance

Directly extends the agentic RL thread that has run through every digest this week — single-agent multi-turn RL methods (AEM, StePPO, ProceedRL, Odysseus, VAGEN) now have a structured multi-agent counterpart. The orchestration-trace framing makes credit assignment in multi-agent settings tractable, and the gap analysis (stopping decision) points to a concrete open problem.

## My Thoughts

<!-- Add your own notes here -->
