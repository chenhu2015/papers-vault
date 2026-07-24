---
title: "OPPO: Bayesian Value Recursion for Token-Level Credit Assignment in LLM Reasoning"
authors: ["Yu Li", "Rui Miao", "Tian Lan", "Zhengling Qi"]
date: 2026-07-24
arxiv_id: "2605.21851"
url: "http://arxiv.org/abs/2605.21851v2"
score: 0.84
topics: [RLHF, RLAIF, GRPO, reward model, agentic RL]
status: unread
---

# OPPO: Bayesian Value Recursion for Token-Level Credit Assignment in LLM Reasoning

## Summary

OPPO shows that the oracle signal used by distillation-style LLM RL methods for local per-token discrimination is precisely the Bayesian update of the model's belief about eventual success; accumulating it along the trajectory yields a closed-form running estimate of success probability at every position, giving a token-level advantage without any learned value network. The factored token-level advantage concentrates credit on genuinely pivotal tokens and provides a directional variance-reduction guarantee. On seven math/science/code benchmarks, OPPO outperforms GRPO, DAPO, and SDPO by up to +6.0 AMC'23 and +5.2 AIME'24 points.

## Key Contributions

- Key insight: oracle per-token discrimination signal = Bayesian update of success probability; accumulating via recursion yields closed-form token-level advantage at the cost of one extra forward pass, no value network required
- Factored advantage form: per-token discrimination signal × state weight — state weight concentrates credit on pivotal tokens, providing directional variance-reduction guarantee
- Two estimators: self-oracle (reuses student model, recovers on-policy distillation reward as special case) and teacher-oracle (stronger frozen model for scoring)
- Unifies distillation-style per-token RL and trajectory-level GRPO within a single Bayesian recursion framework

## Relevance

OPPO partially closes the persistent open gap on unified credit assignment across levels. Where TACO/EGRSD/RL-ZVP operate at the token level using heuristic or entropy-based signals, and GRPO operates at the trajectory level, OPPO provides the first principled Bayesian bridge: trajectory-level success belief propagated backward to individual tokens in closed form. This is structurally complementary to BPO (which reduces variance by sharing trajectory prefixes) and ACPO (which assigns step-level credit via attribution) — OPPO fills the token↔trajectory junction in the credit hierarchy.

## My Thoughts

<!-- Add your own notes here -->
