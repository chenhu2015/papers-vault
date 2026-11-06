---
title: "Grounded Credit Assignment in Reinforcement Learning for Multi-Turn Search Agents"
authors: ["Qirui Liu", "Hao Chen", "Yi Wen", "Weijie Shi", "Yao Zhao", "Xianhe Chen", "Hao Zhao", "Xing Tang", "Weihong Luo", "Yuyu Luo"]
date: 2026-10-16
arxiv_id: "2610.23148v1"
url: "http://arxiv.org/abs/2610.23148v1"
score: 0.85
topics: [agentic RL, GRPO, RL training, LLM agent]
status: unread
---

# Grounded Credit Assignment in Reinforcement Learning for Multi-Turn Search Agents

## Summary

GCA identifies a "grounding gap" in standard GRPO for search agents: Search-R1 improves accuracy but lets evidence-supported correct answers fall from 84.0% to 42.9% on Bamboogle, because GRPO's shared advantage favors memory-based shortcuts over retrieval. GCA separates evidence-retrieval and answer-correctness into verifiable sub-outcomes, applying a correction that penalizes wrong answers more when evidence was found and credits correct answers less when they bypass retrievable evidence. Without extra models or rollouts, GCA raises average EM by 5.7/6.3 points on Qwen2.5-3B/Qwen3-30B-A3B and restores grounding from 76.9% to 93.4%.

## Key Contributions

- Empirically demonstrates the grounding gap: standard GRPO accuracy gains come partly from bypassing retrieval (memory shortcuts)
- Decomposes credit into evidence-finding and answer-correctness sub-outcomes without additional models
- Correction is never negative on evidence-finding search and capped at 10% of token advantage
- +5.7/+6.3 EM improvement at 3B/30B scale; evidence-grounding restored from 76.9% to 93.4%

## Relevance

Directly on the agentic RL + step-credit thread, with an important diagnostic angle: accuracy-only metrics hide quality degradation (grounding collapse) that standard GRPO induces. This pairs well with EG-GRPO (evidence-grounded credit via annotation) and the broader observation from ConCal and SCOPE that credit assignment design fundamentally shapes what the agent learns beyond raw success rates.

## My Thoughts

<!-- Add your own notes here -->
