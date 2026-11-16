---
title: "Teach to Learn: Hint Annealing for Self-improving LLM Reasoning"
authors: ["Zile Wang", "Zijian Li", "Haodong Wang", "Jian Liu", "Qianli Liu", "Lucas Muli", "Blaze Chen", "Song Guo"]
date: 2026-09-28
arxiv_id: "2609.34975v1"
url: "https://arxiv.org/abs/2609.34975"
score: 0.87
topics: [GRPO, RL training, agentic RL, reward model, agentic]
status: unread
---

# Teach to Learn: Hint Annealing for Self-improving LLM Reasoning

## Summary

HATCH (Hint-Annealed Self-Teaching) addresses GRPO's zero-gradient problem on hard queries by injecting self-generated hints to recover reward contrast, then mitigating hinted reward shift via online weighting that anneals hinted trajectories' contribution over training. Gradient projection removes the conflicting component of hint-generation updates relative to the query-solving objective, enabling a single policy to both create and exploit its own learning opportunities. Outperforms state-of-the-art by 1.02–4.32 pp on Llama-3.2-1B and Qwen3-1.7B/8B.

## Key Contributions

- Identifies "hinted reward shift": hint-based recovery concentrates policy updates on hinted trajectories, limiting improvement without hints
- Online weighting anneal: reduces hinted trajectory weight progressively to prevent over-reliance on assisted mode
- Gradient projection: removes component of hint-generation gradient that opposes query-solving objective
- Single-policy framework — no separate teacher model; policy generates, uses, and benefits from its own hints

## Relevance

Directly in the adaptive scaffolding cluster (8th entry) with a novel dimension: HATCH is the first entry that uses gradient projection to resolve the conflict between the hint-generation and query-solving objectives within a single policy. The hinted reward shift diagnosis also adds a new failure-mode analysis to the zero-advantage collapse cluster (PICO, Scaf-GRPO, BRAT): hint injection can trade the zero-reward collapse for a different degenerate attractor where the policy only solves queries when hinted.

## My Thoughts

<!-- Add your own notes here -->
