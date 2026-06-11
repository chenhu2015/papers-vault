---
title: "Policy-Conditioned Counterfactual Credit for Verifiable Reinforcement Learning of Long-Horizon Language Agents"
authors: ["Renwei Meng"]
date: 2026-06-11
arxiv_id: "2606.05263v1"
url: "http://arxiv.org/abs/2606.05263v1"
score: 0.80
topics: [agentic RL, reward model, RL training, LLM agent]
status: unread
---

# Policy-Conditioned Counterfactual Credit for Verifiable Reinforcement Learning of Long-Horizon Language Agents

## Summary

Long-horizon language agents trained with verifiable rewards learn correlational shortcuts: steps that resemble retrieval or verification but do not causally contribute to the verified outcome. CVT-RL introduces a policy-conditioned counterfactual contribution (PCCC) estimator using four controlled intervention types — deletion, semantic substitution, evidence substitution, and tool-output perturbation — with doubly-robust advantage augmentation, plus an augmented Lagrangian constraining unsupported claims, skipped verification, and tool tampering. On long-context QA, ALFWorld, ScienceWorld, and web/tool tasks, CVT-RL improves average task success from 71.8% to 78.9% and reduces measured reward hacking from 7.2% to 3.9% versus non-causal RL baselines.

## Key Contributions

- Policy-conditioned counterfactual contribution (PCCC) estimator with 4 intervention types: deletion, semantic substitution, evidence substitution, tool-output perturbation
- Doubly-robust advantage augmentation with selection-adjusted estimator; frozen reference policy samples continuations
- Augmented Lagrangian constraining unsupported claims, skipped verification, tool tampering, unsafe calls
- 78.9% task success (+7.1pp vs non-causal RL), reward hacking 3.9% vs 7.2%; adaptive evasion attacks only raise hacking to 7.1%

## Relevance

Extends CERL (Jun 10 runner-up) from persistent-state counterfactuals to a general 4-type intervention framework. Directly addresses the reward hacking thread (HARVE Jun 8) from a causal angle rather than mechanistic editing: CVT-RL prevents shortcut formation during training rather than removing it post-hoc from the reward head.

## My Thoughts

<!-- Add your own notes here -->
