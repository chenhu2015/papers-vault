---
title: "Learning When to Plan: Efficiently Allocating Test-Time Compute for LLM Agents"
authors: ["Davide Paglieri", "Bartlomiej Cupial", "Jonathan Cook", "Ulyana Piterbarg", "Jens Tuyls", "Edward Grefenstette", "Jakob Nicolaus Foerster", "Jack Parker-Holder", "Tim Rocktaschel"]
date: 2025-09-03
arxiv_id: "2509.03581"
url: "https://arxiv.org/abs/2509.03581"
score: 0.74
topics: [agentic RL, RL training, LLM agent]
status: unread
---

# Learning When to Plan: Efficiently Allocating Test-Time Compute for LLM Agents

## Summary

Proposes dynamic planning for LLM agents via a two-stage pipeline: SFT on synthetic data primes the model for dynamic planning decisions, then RL refines the capability in long-horizon environments (Crafter). The core finding is that always-planning is computationally wasteful and degrades long-horizon task performance, while never-planning limits complex task success — dynamic allocation via RL finds the optimal compute allocation. A secondary finding is that agents trained this way can be steered by human-written plans, suggesting structured human-AI collaboration potential.

## Key Contributions

- Formal framework for dynamic planning: agent decides when to invoke explicit planning compute vs. acting directly
- Two-stage training: SFT on diverse synthetic dynamic-planning traces to establish prior, then RL in Crafter to refine via long-horizon feedback
- Always-planning degrades long-horizon performance because it consumes context and disrupts action execution; dynamic allocation avoids this
- Human-plan steering as a zero-shot capability: agents can execute user-provided plans beyond their independent capabilities

## Relevance

Structurally echoes Learning When to Plan (Shen et al.) and RSPO's insight: compute should be allocated selectively, not uniformly. Here the unit is planning invocations rather than reflection steps or reward density. The SFT→RL two-stage pipeline mirrors the broader vault pattern of warm-starting RL with SFT data (VRRL, SVR-R1's SFT base). The human-steering capability is the most novel finding for practical agentic RL — it suggests that RL-trained dynamic planners are more steerable by human guidance than always-planning agents.

## My Thoughts

<!-- Add your own notes here -->
