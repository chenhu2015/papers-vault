---
title: "Internalizing Curriculum Judgment for LLM Reinforcement Fine-Tuning"
authors: ["Han Zheng", "Yining Ma", "Karthick Gunasekaran", "Bharathan Balaji", "Zheng Du", "Shiv Vitaladevuni", "Cathy Wu"]
date: 2026-05-11
arxiv_id: "2605.11235v1"
url: "http://arxiv.org/abs/2605.11235v1"
score: 0.87
topics: [RL training, agentic RL, reinforcement learning, GRPO, LLM agent]
status: unread
---

# Internalizing Curriculum Judgment for LLM Reinforcement Fine-Tuning

## Summary

METIS internalizes curriculum judgment as a native model capability rather than relying on external heuristics: it observes that within-prompt reward variance gauges informativeness, then trains the model to predict this variance from recent training history as lightweight in-context examples, dynamically controlling training allocation. A joint self-judgment reward closes the metacognitive loop so the policy learns what to learn next. Across math, code generation, and agentic function-calling benchmarks, METIS delivers superior performance while accelerating convergence by up to 67%.

## Key Contributions

- Identifies within-prompt reward variance as a reliable proxy for prompt informativeness in RLVR training
- METIS framework: model predicts its own reward variance from recent outcomes as in-context examples (no auxiliary model needed)
- Self-judgment reward jointly optimized with standard RFT rewards, enabling metacognitive self-curriculum
- Tested across discrete and continuous RFT benchmarks: math, code generation, and agentic function-calling
- Up to 67% convergence speedup over standard curriculum-agnostic RLVR training

## Relevance

This directly extends the reward-variance-as-difficulty-signal insight (related to VCRL from search 3) but goes further by internalizing that judgment inside the model itself, eliminating auxiliary curriculum schedulers. Highly relevant to the RL training and agentic RL core interests, particularly the agentic function-calling evaluation which ties into LLM agent keyword.

## My Thoughts

<!-- Add your own notes here -->
