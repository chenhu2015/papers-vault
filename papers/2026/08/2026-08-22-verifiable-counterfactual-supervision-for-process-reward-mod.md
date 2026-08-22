---
title: "Verifiable Counterfactual Supervision for Process Reward Models"
authors: ["Yinghui Chi", "Yuanhong Wang"]
date: 2026-08-22
arxiv_id: "2605.02395v3"
url: "https://arxiv.org/abs/2605.02395"
score: 0.82
topics: [reward model, RLAIF, reinforcement learning, agentic RL]
status: unread
---

# Verifiable Counterfactual Supervision for Process Reward Models

## Summary

This paper operationalises the counterfactual ground truth that "Credit Without Ground Truth" (Aug 21) showed was missing from all standard step-level credit signals. Starting from a verified symbolic reasoning chain, it injects a template-aware error at a selected step, recomputes all subsequent steps under the corrupted state, and verifies that the injected step is not derivable from its prefix — producing prefix-valid first-error annotations. PRMs trained on this synthetic data improve Best-of-8 reranking on logical reasoning benchmarks and show preliminary transfer to mathematical process evaluation.

## Key Contributions

- **Verifiable counterfactual framing**: defines the supervision requirement as prefix-valid first-error annotation — the error must be injected at a specific step, the injected step must not be derivable from its prefix, and subsequent steps must be coherent under the corrupted state
- **Template-aware error injection**: symbolic reasoning chain templates allow controlled, targeted error insertion at any selected intermediate step
- **Coherent corruption**: the entire suffix is recomputed under the corrupted state, ensuring the trajectory is internally consistent after injection
- **Empirical validation**: Best-of-8 reranking improvements on logical reasoning; preliminary positive transfer to mathematical process evaluation

## Relevance

"Credit Without Ground Truth" (Aug 21, score 0.91) was the highest-scoring paper in that digest and opened the meta-gap: if no standard step-level signal identifies causally important steps better than chance, what would a *verifiable* signal look like? This paper provides a direct constructive answer. The template-aware counterfactual approach is the closest thing in the vault to the causal counterfactual methodology "Credit Without Ground Truth" used as ground truth — but applied to PRM training rather than auditing. Together these two papers define both the problem and a proposed solution path for the causal credit assignment thread.

## My Thoughts

<!-- Add your own notes here -->
