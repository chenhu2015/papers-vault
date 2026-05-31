---
title: "Reward Bias Substitution: Single-Axis Bias Mitigations Redirect Optimization Pressure"
authors: ["Max Lamparth", "Daniel Fein", "Andreas Haupt", "Marcel Hussing", "Mykel J. Kochenderfer"]
date: 2026-05-31
arxiv_id: "2605.27996"
url: "https://arxiv.org/abs/2605.27996"
score: 0.88
topics: [RLHF, reward model, GRPO, RL training]
status: unread
---

# Reward Bias Substitution: Single-Axis Bias Mitigations Redirect Optimization Pressure

## Summary

Single-axis mitigation of reward model biases (length, sycophancy, style) rotates optimization pressure onto correlated proxies rather than eliminating it — formalized as "reward bias substitution". The paper proves this failure mode is invisible to any audit-distribution metric including ranking accuracy and win-rate even with oracle reward access, and demonstrates empirically that a length penalty during GRPO training compresses responses as intended but redirects optimization toward overconfidence, degrading factual accuracy.

## Key Contributions

- Formalizes reward bias substitution: single-axis mitigation shifts pressure to correlated proxies, undetectable under any audit distribution even with oracle reward
- Proves that successful mitigation, bias substitution, and overcorrection produce identical observables, closing the measurement-versus-optimization gap only by tracking multiple biases on policy-induced distributions
- Demonstrates empirically: GRPO length penalty compresses responses but induces overconfidence and factual accuracy drop; published length-debiasing operator reintroduces bias under best-of-N selection on 3 of 4 SOTA reward models
- Provides actionable prescriptions: evaluate on policy-induced distributions, track multiple bias axes simultaneously

## Relevance

This paper directly resolves the long-standing reward model OOD carry-forward (May 29–30): it shows why single-axis reward fixes in RLHF systematically fail, which is the core of reward overoptimization. The GRPO empirical demonstration makes it directly actionable for understanding reward hacking dynamics in LLM RL.

## My Thoughts

<!-- Add your own notes here -->
