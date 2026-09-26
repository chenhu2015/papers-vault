---
title: "Reinforcement Learning with Verifiable Rewards for Small Search Agents"
authors: ["Gaurisankar Jayadas", "Aske Plaat", "Álvaro Serra-Gómez", "Sandheep P"]
date: 2026-09-23
arxiv_id: "2609.28765"
url: "https://arxiv.org/abs/2609.28765"
score: 0.78
topics: [RLHF, RLAIF, GRPO, agentic, tool use, LLM agent]
status: unread
---

# Reinforcement Learning with Verifiable Rewards for Small Search Agents

## Summary

This paper tests GRPO with a Wikipedia search tool on the small Qwen3.5-0.8B model on multi-hop QA, finding that RLVR works for sub-1B models without teacher distillation (3.8x gain over untrained). Critically, it shows that reward shape is decisive for small models: the sparse exact-match reward standard in math/code RLVR is the worst-performing shape across all seeds, suggesting small-model agentic RLVR requires its own reward design study rather than a scaled-down copy of large-model recipes.

## Key Contributions

- First demonstration that RLVR (GRPO) works for sub-1B parameter models on agentic search tasks without distillation
- Reward shape comparison across three formulations: sparse exact-match (worst), and two richer alternatives
- Finding that the standard sparse exact-match reward, despite directly optimizing the eval metric, underperforms at small scale
- Evidence that the reason-over-search GRPO recipe generalizes across model sizes given appropriate reward design

## Relevance

Connects to the reward design thread (Spurious Tool Use, EAPO) but from an efficiency angle: what reward works for small models doing tool use? The negative result on sparse exact-match reward echoes earlier findings on reward pathologies in agentic settings, and the 0.8B scale points toward practical deployment without large compute budgets.

## My Thoughts

<!-- Add your own notes here -->
