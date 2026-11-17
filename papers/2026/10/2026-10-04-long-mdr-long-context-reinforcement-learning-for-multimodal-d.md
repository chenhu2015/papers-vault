---
title: "Long-MDR: Long-Context Reinforcement Learning for Multimodal Deep-Research Agents"
authors: ["On Tai Tang", "Huanyao Zhang", "Jiepeng Zhou", "Wentao Zhang"]
date: 2026-10-04
arxiv_id: "2610.05195"
url: "https://arxiv.org/abs/2610.05195"
score: 0.85
topics: [multimodal models, vision language models, VLM, LLM agent, agentic, tool use]
status: unread
---

# Long-MDR: Long-Context Reinforcement Learning for Multimodal Deep-Research Agents

## Summary

First online RL study training a multimodal research agent at 128k context and 75+ tool-interaction turns; identifies three failure modes at this scale (weak early policy wastes large interaction budgets; entropy collapse before performance saturates) and addresses them with three techniques: OPD Warmup (distill a strong teacher before RL), Progressive Horizon Expansion (incrementally increase the tool-turn budget), and Entropy-Triggered Rescue (detect and correct entropy collapse mid-training). Demonstrates continued performance gains in a regime where direct RL training is otherwise slow and unstable.

## Key Contributions

- First online multimodal RL trained at 128k context with 75+ tool-turn horizon
- OPD Warmup: on-policy distillation from a strong teacher before RL fine-tuning, establishing a competent starting policy
- Progressive Horizon Expansion: incrementally increasing the tool-turn budget to prevent early-policy waste of large interaction budgets
- Entropy-Triggered Rescue: mid-training detection of entropy collapse with active rescue to prevent premature learning termination

## Relevance

Directly extends the agentic VLM cluster (Reframe, Nov 15) to the extreme scale regime. The OPD Warmup technique connects to the multi-turn OPD cluster (SAGE-OPD Nov 16, Skill-SD today) — using distillation as a training stabilizer before RL rather than as a training signal alongside RL. The progressive horizon + entropy rescue techniques are novel engineering contributions to the multi-turn agentic RL training toolbox. This paper also validates the importance of the OPSD/OPD techniques found in the Nov 15–16 searches.

## My Thoughts

<!-- Add your own notes here -->
