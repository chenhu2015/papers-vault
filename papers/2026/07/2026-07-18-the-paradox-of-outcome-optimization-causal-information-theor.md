---
title: "The Paradox of Outcome Optimization: A Causal Information-Theoretic Bound on Reasoning Shortcuts in LLMs"
authors: ["Zihan Chen", "Yiming Zhang", "Wenxiang Geng", "Zenghui Ding", "Yining Sun"]
date: 2026-05-30
arxiv_id: "2606.00674"
url: "https://arxiv.org/abs/2606.00674"
score: 0.82
topics: [RLHF, reward model, RL training, reinforcement learning, agentic RL]
status: unread
---

# The Paradox of Outcome Optimization: A Causal Information-Theoretic Bound on Reasoning Shortcuts in LLMs

## Summary

Establishes a theoretical framework bridging Structural Causal Models (SCM) and the Information Bottleneck (IB) principle to explain Reward-Induced Manifold Collapse — why outcome-RL-trained LLMs achieve strong benchmark performance but brittle OOD reasoning. Shows that SGD optimization biases models toward low-complexity shortcut solutions when training distributions allow Markovian Screening of the true causal mechanism, and derives a generalization bound based on Semantic Coverage Measure (η) rather than sample size. Formally establishes PRMs as Topological Filters enforcing step-wise mutual information constraints that render shortcut manifolds inadmissible — the first mathematical grounding for why PRMs improve OOD generalization beyond simple credit assignment.

## Key Contributions

- Formalizes Reward-Induced Manifold Collapse: outcome-RL models learn shortcut solutions when the training distribution allows Markovian Screening of true causal reasoning chains
- Derives generalization bound based on Semantic Coverage Measure (η) — explains why scaling homogeneous data fails to fix reasoning brittle-ness: coverage, not quantity, determines bound tightness
- PRMs as Topological Filters: step-wise MI constraints enforce that the shortcut manifold becomes inadmissible, providing the first formal explanation for why PRMs improve OOD generalization
- Bridges three previously separate literatures: causal inference (SCM), information theory (IB), and RL for reasoning (PRMs, RLVR)

## Relevance

Provides the missing theoretical complement to the vault's empirical PRM thread (GroundedPRM, KV-PRM, SCI-PRM, LLMs-as-a-Jury). Prior vault papers showed PRMs improve performance; this paper explains *why* they improve OOD generalization. The Semantic Coverage Measure bound also suggests a new direction for the confirmed open gap: if sample diversity (coverage) matters more than quantity, then data curation for RLVR training is more critical than data scale — a thread the vault has not yet searched.

## My Thoughts

<!-- Add your own notes here -->
