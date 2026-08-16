---
title: "The Horizon Gap: Planning, Memory, Execution, Training, and Evaluation for Long-Horizon LLM Agents"
authors: ["Mingguang Chen", "Licheng Wang", "Bo Qu"]
date: 2026-08-07
arxiv_id: "2608.06663v1"
url: "https://arxiv.org/abs/2608.06663"
score: 0.82
topics: [agentic RL, LLM agent, reinforcement learning]
status: unread
---

# The Horizon Gap: Planning, Memory, Execution, Training, and Evaluation for Long-Horizon LLM Agents

## Summary

This 1,547-paper survey of long-horizon LLM agent research (2024–2026) introduces a three-property distinction — long-horizon (task steps), long-context (token capacity), and long-term memory (cross-session persistence) — to disambiguate three routinely conflated concepts. The survey organizes findings into six lifecycle categories (planning, memory, execution, training, evaluation, foundations/safety) and finds field-wide convergence toward dense step-level signals as the response to uninformative outcome-only supervision. Open measurement problems include decomposing model vs. harness capability and managing correlated bias in process-level signals used simultaneously for training and evaluation.

## Key Contributions

- Three-property taxonomy disambiguating long-horizon (task), long-context (model), and long-term memory (system) — ending conflation that muddies benchmark comparisons
- Six-category lifecycle framework (planning → memory → execution → training → evaluation → foundations/safety) with a within/beyond/cross-context axis
- Field-wide diagnosis: outcome-only signals grow uninformative as horizons lengthen; field responds universally by manufacturing denser step-level signals (PRM, CA, trajectory diagnostics)
- Open measurement problems: model-vs-harness capability decomposition and correlated bias in process-level signals used for both training and evaluation

## Relevance

This survey independently validates the vault's agentic RL credit assignment and process reward threads at the 1,547-paper scale, directly mapping onto the vault's open gaps (process reward correlated bias is Gap #19's calibration problem applied to evaluation; model-vs-harness decomposition is a formal question the vault's PASS@(k,T) paper below also addresses). The CA survey (2604.09459v3, Aug 13) confirmed the vault's credit taxonomy; the Horizon Gap confirms the vault's step-level signal framing.

## My Thoughts

<!-- Add your own notes here -->
