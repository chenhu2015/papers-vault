---
title: "Rethinking RL for LLM Reasoning: It's Sparse Policy Selection, Not Capability Learning"
authors: ["Ömer Faruk Akgül", "Rajgopal Kannan", "Willie Neiswanger", "Viktor Prasanna"]
date: 2026-05-07
arxiv_id: "2605.06241v2"
url: "http://arxiv.org/abs/2605.06241v2"
score: 0.78
topics: [reinforcement learning, RL training, GRPO, LLM agent]
status: unread
---

# Rethinking RL for LLM Reasoning: It's Sparse Policy Selection, Not Capability Learning

## Summary

Token-level analysis across multiple model families and RL algorithms finds that RL's beneficial footprint concentrates at 1-3% of token positions — specifically high-entropy decision branching points — where the promoted token always lies within the base model's top-5 alternatives. Targeted corrections at only those entropy-gated positions causally recover a large fraction of RL's accuracy gain, motivating ReasonMaxxer: an RL-free method that applies contrastive loss at entropy-gated points using a few hundred base-model rollouts, matching full RL performance with ~1000x training cost reduction.

## Key Contributions

- Empirical finding: RL modifies only 1-3% of tokens, always within base model's top-5 alternatives at those positions
- Causal verification that entropy-gated high-uncertainty positions drive RL's accuracy gain
- ReasonMaxxer: contrastive loss at entropy-gated decision points, RL-free, minutes of single-GPU training
- "Sparse policy selection" framing reframes RL-for-reasoning as redistribution rather than capability acquisition

## Relevance

This paper provides the unifying empirical theory connecting AT-RL (Jun 14, ~15% of MLLM tokens are high visual-textual anchors), ConSteer-RL (Jun 9, steering reasoning at entropy pivots), and ProFIL (Jun 20, zeroing advantage for post-commitment theater after entropy-driven commitment point). All three are consequences of the same underlying structure: effective RL intervention is sparse and concentrated at high-entropy branching positions. The "sparse policy selection, not capability learning" framing also provides a concrete mechanism for the First-Principles paper's (Jun 16) theoretical prediction that "RL recombines, SFT covers" — RL cannot create new capabilities because it only selects among what the base model already knows at uncertainty points.

## My Thoughts

<!-- Add your own notes here -->
