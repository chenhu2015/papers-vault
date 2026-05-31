---
title: "TRACER: Turn-level Regret Matching with Inner Reinforcement Credit for Cooperative Multi-LLM Reasoning"
authors: ["Chusen Li", "Zhou Liu", "Shuigeng Zhou", "Wentao Zhang"]
date: 2026-05-31
arxiv_id: "2605.28699"
url: "https://arxiv.org/abs/2605.28699"
score: 0.83
topics: [agentic RL, GRPO, multi-agent, LLM agent, RL training]
status: unread
---

# TRACER: Turn-level Regret Matching with Inner Reinforcement Credit for Cooperative Multi-LLM Reasoning

## Summary

TRACER separates cooperative multi-LLM reasoning into a controller-regret layer — using game-theoretic regret matching to decide whether agents speak or skip — and a generation-credit layer applying role-specific GSPO rewards to proposer and reviewer utterances. This two-level structure eliminates free-riding and sparse rewards while extending classical regret matching to provably convergent deep RL for multi-agent LLM training, evaluated on GSM8K, MATH500, and GPQA-Diamond.

## Key Contributions

- Two-layer design: controller-regret layer (regret matching for speak/skip binary action) + generation-credit layer (role-specific GSPO for utterance quality)
- Extends classical finite-action-space regret matching to deep learning with provable convergence guarantees
- Avoids free-riding by assigning credit at both action-mode and utterance levels; reduces training compute by expanding only controller choices
- Evaluated on GSM8K, MATH500, and GPQA-Diamond, measuring in-domain accuracy, generalization, inference cost, and correction-preservation

## Relevance

Opens the underexplored multi-agent LLM RL thread (only CoRe-Code from May 29 had touched this). The GSPO reward is a GRPO variant making this directly relevant to the RL training methodology the user follows, and the game-theoretic regret matching provides a principled alternative to fixed debate/voting protocols.

## My Thoughts

<!-- Add your own notes here -->
