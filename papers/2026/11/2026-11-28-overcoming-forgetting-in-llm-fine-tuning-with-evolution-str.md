---
title: "Overcoming Forgetting in LLM Fine-Tuning with Evolution Strategies"
authors: ["Kajetan Schweighofer", "Conor F. Hayes", "Roberto Dailey", "Risto Miikkulainen", "Xin Qiu"]
date: 2026-05-28
arxiv_id: "2605.30148"
url: "https://arxiv.org/abs/2605.30148"
score: 0.78
topics: [RL training, reinforcement learning, agentic RL]
status: unread
---

# Overcoming Forgetting in LLM Fine-Tuning with Evolution Strategies

## Summary

This paper examines forgetting in ES-based LLM fine-tuning and finds it is better characterised as reversible performance drift rather than catastrophic forgetting — prior-task performance often recovers during continued ES training — and that forgetting is not specific to ES but also appears in gradient-based methods. The authors propose mitigation strategies that substantially reduce drift without sacrificing new-task gains, strengthening the case for ES as a practical alternative to RL-based fine-tuning. This directly extends the ARS-VLM + "Dimension Is Free" ES thread by addressing its main reported weakness.

## Key Contributions

- Reframes ES forgetting as performance drift (reversible) rather than catastrophic forgetting (irreversible) — a qualitative distinction with practical implications
- Shows that gradient-based fine-tuning also exhibits this drift, so forgetting is not an ES-specific failure mode
- Proposes mitigation strategies (not ES-specific) that reduce drift while preserving new-task performance gains
- Strengthens the ES vs. RL fine-tuning comparison by removing what had been the primary ES disadvantage

## Relevance

Directly addresses the main open weakness of the ES-for-LLMs thread. ARS-VLM showed 7.5× step reduction vs GRPO; "Dimension Is Free" predicted ES outperforms GRPO on long-horizon tasks; PBPT applied population-based training to RLVR. This paper completes the ES picture by showing that the "forgetting" objection to ES is overstated and applies equally to gradient methods.

## My Thoughts

<!-- Add your own notes here -->
