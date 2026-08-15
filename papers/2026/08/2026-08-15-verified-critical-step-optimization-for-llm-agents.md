---
title: "Verified Critical Step Optimization for LLM Agents"
authors: ["Mukai Li", "Qingcheng Zeng", "Tianqing Fang", "Zhenwen Liang", "Linfeng Song", "Qi Liu", "Haitao Mi", "Dong Yu"]
date: 2026-08-15
arxiv_id: "2602.03412"
url: "http://arxiv.org/abs/2602.03412v2"
score: 0.76
topics: [agentic RL, LLM agent, reward model, RL training, tool use]
status: unread
---

# Verified Critical Step Optimization for LLM Agents

## Summary

CSO focuses preference learning (DPO) exclusively on verified critical steps—decision points where the agent's alternate action demonstrably flips the task from failure to success—rather than applying supervision uniformly across steps or outcomes. The verification pipeline uses a PRM to identify candidate critical steps, expert models to propose high-quality alternatives, then the policy itself to execute those alternatives to completion; only alternatives that reach correct outcomes are used as DPO training data. On GAIA and XBench-DeepSearch, CSO achieves 37% and 26% relative improvement over SFT baselines while requiring supervision at only 16% of trajectory steps.

## Key Contributions

- Defines "critical steps" as decision points where alternate actions flip task outcomes from failure to success—a new credit assignment granularity finer than step-level
- Three-stage verification: PRM identification → expert alternative generation → policy self-execution to completion (reachability filter)
- DPO on only verified critical steps; avoids trajectory-level coarseness and step-level noise simultaneously
- 37%/26% relative gain on GAIA-Text-103/XBench-DeepSearch with supervision at 16% of steps

## Relevance

CSO's critical step identification (outcome-flipping decision points) is structurally related to SHAPE's solvability-potential estimation (steps that determine which trajectory segment is solvable) and to the CA survey's six-diagnostic framework for agentic credit. The policy self-execution reachability requirement is novel: CSO only trains on alternatives the policy can actually reach, directly addressing the distribution shift problem that makes Monte Carlo step rewards unreliable. This is an empirical complement to TCRM's theoretical TD regularization for reward models—both aim to make step-level signals reflect genuine expected future outcomes.

## My Thoughts

<!-- Add your own notes here -->
