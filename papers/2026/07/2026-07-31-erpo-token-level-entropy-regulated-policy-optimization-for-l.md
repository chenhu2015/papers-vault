---
title: "ERPO: Token-Level Entropy-Regulated Policy Optimization for Large Reasoning Models"
authors: ["Song Yu", "Li Li", "Wenwen Zhao", "Zhisheng Yang"]
date: 2026-07-31
arxiv_id: "2603.28204"
url: "https://arxiv.org/abs/2603.28204"
score: 0.82
topics: [agentic RL, RL training, GRPO, reward model]
status: unread
---

# ERPO: Token-Level Entropy-Regulated Policy Optimization for Large Reasoning Models

## Summary

ERPO identifies Critical Decision Pivots (CDPs) — transient high-entropy states where the policy's trajectory is most sensitive to perturbations — and diagnoses these as the locations where uniform GRPO advantage suppresses effective multi-path exploration. Three synergistic components address this: entropy-aware gating that amplifies exploration at CDPs, bucket-based implicit normalization that corrects difficulty bias by aligning token progress windows, and result-anchored advantage synthesis that re-weights token signals via outcome-driven anchors. Significantly outperforms GRPO on mathematical benchmarks while producing more concise and robust reasoning paths.

## Key Contributions

- Critical Decision Pivots (CDPs): high-entropy states identified as trajectory-sensitive forks where uniform advantage actively suppresses exploration
- Entropy-aware gating: amplifies effective advantage at CDPs to promote diverse path discovery
- Bucket-based implicit normalization: corrects difficulty bias by grouping tokens into progress windows for normalization
- Result-anchored advantage synthesis: re-weights token-level signals by outcome-driven anchors, addressing the trajectory-vs-token advantage mismatch

## Relevance

ERPO's CDP concept is the same entropy-as-structural-signal pattern as STAPO, O²-CritiCuRL, TAO-RL, and STARE (Gap #12), but names it explicitly as a decision-theoretic concept ("forks in the road") rather than a variance/surprisal metric. The three-component synthesis (entropy gating + difficulty normalization + outcome anchoring) is the most compositionally complete approach in the vault for token-level credit assignment under GRPO, combining elements from separate papers: entropy gating (STAPO/STARE), difficulty normalization (RDPO/bucket), and outcome anchoring (result-anchored). From March 2026, predating STARE and TAO-RL.

## My Thoughts

<!-- Add your own notes here -->
