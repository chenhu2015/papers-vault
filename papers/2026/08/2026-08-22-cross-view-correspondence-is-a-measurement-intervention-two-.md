---
title: "Cross-View Correspondence Is a Measurement Intervention: Two-Sided Validation for Agent Evaluation and Credit Assignment"
authors: ["Zhen Zhang", "Ahmad Hafez", "Amr Alanwar"]
date: 2026-08-22
arxiv_id: "2608.17713v1"
url: "https://arxiv.org/abs/2608.17713"
score: 0.78
topics: [agentic RL, LLM agent, reward model, reinforcement learning]
status: unread
---

# Cross-View Correspondence Is a Measurement Intervention: Two-Sided Validation for Agent Evaluation and Credit Assignment

## Summary

This paper develops a validity theory for the correspondence step used in cross-view agent evaluation and trace-based credit assignment, showing it is a measurement intervention — not neutral preprocessing — that can manufacture sensitivity or invariance and leave signed learning credit unidentified when multiple optimal correspondences exist. Empirically, two deterministic optimal tracebacks disagree on temporal localisation for 55.9% of nonzero trajectory pairs across public code/SQL pipelines; frozen tool-use audits show exact-optimum reversals of intended turn-level credit. Cross-view correspondence must be declared, validated, and its uncertainty propagated before any point conclusion about credit.

## Key Contributions

- **Measurement intervention framing**: establishes that cross-view correspondence is an active intervention that can manufacture sensitivity (false positives) or invariance (false negatives), not a neutral preprocessing step
- **Two-sided validation framework**: requires both nuisance removal *and* response preservation to be verified; a map that passes one test can fail the other
- **All-optima identification**: sharp ranges computed over the full set of exact-optimum correspondences; a credit coordinate is retained only when all exact optima agree on its nonzero sign
- **Empirical finding**: 55.9% disagreement rate between two deterministic tracebacks on turn-level credit in 1,586 nonzero trajectory pairs; exact-optimum reversals of intended credit in frozen tool-use audits

## Relevance

This paper speaks directly to the causal credit assignment meta-gap opened by "Credit Without Ground Truth" (Aug 21). Where that paper showed that existing step-level credit *signals* don't correlate with causal contribution, this paper shows that even the *measurement procedure* for assigning credit across views of an agent's trajectory is not well-defined — two optimal correspondence procedures can disagree on which turns caused success. Every vault paper that uses turn-level credit assignment (RTPO, PlanPO, MileGPO, SkillGate) implicitly relies on a fixed correspondence that may not be the only optimal one.

## My Thoughts

<!-- Add your own notes here -->
