---
title: "Dependency-Aware Trajectory Refinement for Efficient Multi-Turn Agent Fine-Tuning"
authors: ["Zhuo Chen", "Zhen Zhang", "Xinyu Wang", "Kewei Tu"]
date: 2026-09-16
arxiv_id: "2609.18417v1"
url: "http://arxiv.org/abs/2609.18417v1"
score: 0.74
topics: [agentic RL, LLM agent, tool use]
status: unread
---

# Dependency-Aware Trajectory Refinement for Efficient Multi-Turn Agent Fine-Tuning

## Summary

This work models multi-turn agent trajectories as round-level dependency DAGs that identify which rounds are globally load-bearing for the final answer, then fine-tunes agents on trajectories refined by removing non-load-bearing rounds. Training on refined trajectories improves accuracy by up to 1.7 pp over vanilla SFT and 5.7 pp over an LLM-deletion baseline, while reducing inference messages by ~40% and tokens by ~48%. The DAG structure provides a principled, interpretable alternative to heuristic round-pruning for agent trajectory efficiency.

## Key Contributions

- Round-level dependency DAG: LLM-annotated graph exposing global load-bearing rounds vs redundant rounds (failed tool calls, parallel sub-queries, verification-only steps)
- Deterministic and interpretable trajectory refinement: edits are structurally derived, not model-guessed
- Optional rephrasing for removed rounds improves coherence of refined trajectories
- Consistent accuracy gains on four multi-modal QA benchmarks with substantial inference cost reduction

## Relevance

Addresses the trajectory efficiency thread adjacent to STRIDE/RetireOPD (Sep 18 vault): where STRIDE and RetireOPD accelerate on-policy distillation by stopping early, this paper prunes the training trajectory itself using causal dependency structure. The DAG framing is complementary to BATON's trajectory mass normalization — both ask which parts of a trajectory carry the learning signal, but at the structure (DAG) vs weight (mass) levels respectively.

## My Thoughts

<!-- Add your own notes here -->
