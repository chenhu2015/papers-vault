---
title: "Rewarding Beliefs, Not Actions: Consistency-Guided Credit Assignment for Long-Horizon Agents"
authors: ["Wenjie Tang", "Minne Li", "Sijie Huang", "Liquan Xiao", "Yuan Zhou"]
date: 2026-05-22
arxiv_id: "2605.20061"
url: "https://arxiv.org/abs/2605.20061"
score: 0.84
topics: [agentic RL, LLM agent, GRPO, reward model]
status: unread
---

# Rewarding Beliefs, Not Actions: Consistency-Guided Credit Assignment for Long-Horizon Agents

## Summary

ReBel addresses temporal credit assignment in partially observable long-horizon LLM agent tasks by explicitly modeling structured belief states to summarize interaction history, with belief-consistency supervision that converts discrepancies between predicted beliefs and observed feedback into dense self-supervised signals without requiring external step-wise annotations. Belief-aware grouping compares trajectories under similar belief states for more robust, lower-variance advantage estimates. Evaluated on ALFWorld and WebShop, improving task success by up to 20.4 percentage points over GRPO with 2.1× better sample efficiency.

## Key Contributions

- Belief-state modeling for LLM agents: structured belief states summarize interaction history and guide policy learning in partially observable environments
- Belief-consistency supervision: prediction/feedback discrepancies become dense self-supervised reward signals without external step-level annotation
- Belief-aware grouping: advantage estimation compares trajectories under similar belief states, reducing variance vs. standard GRPO
- +20.4 pp over GRPO on ALFWorld, 2.1× sample efficiency improvement on WebShop

## Relevance

Extends the agentic RL + long-horizon credit assignment thread (SOLAR-RL May 17, PAIR May 19, CEPO May 20) with a novel belief-state framing inspired by POMDP theory. Unlike step-level reward methods (SRaR, MoCA) that need annotation or a verifier, ReBel generates dense signals from belief-prediction consistency — a self-supervised alternative for partial observability.

## My Thoughts

<!-- Add your own notes here -->
