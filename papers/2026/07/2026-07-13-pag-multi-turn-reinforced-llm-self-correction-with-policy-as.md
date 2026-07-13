---
title: "PAG: Multi-Turn Reinforced LLM Self-Correction with Policy as Generative Verifier"
authors: ["Yuhua Jiang", "Yuwen Xiong", "Yufeng Yuan", "Chao Xin", "Wenyuan Xu", "Yu Yue", "Qianchuan Zhao", "Lin Yan"]
date: 2026-07-13
arxiv_id: "2506.10406v1"
url: "https://arxiv.org/abs/2506.10406"
score: 0.82
topics: [agentic RL, RL training, GRPO, reward model, LLM agent]
status: unread
---

# PAG: Multi-Turn Reinforced LLM Self-Correction with Policy as Generative Verifier

## Summary

PAG (Policy as Generative Verifier) enables LLMs to self-correct by alternating between policy and verifier roles within a unified multi-turn RL paradigm, using a selective revision mechanism that only triggers a second attempt when the model's own generative verification detects an error. This verify-then-revise workflow reduces model collapse while jointly improving both reasoning accuracy and verification quality. Unlike approaches that always generate a second attempt, the selective mechanism allocates test-time compute only where the model is uncertain.

## Key Contributions

- Unified multi-turn RL framework where the same model alternates between policy (generate solution) and verifier (check solution) roles
- Selective revision: only revises when generative verification detects an error — avoids wasted compute on correct-but-revised answers
- Jointly enhances both direct generation accuracy and self-verification accuracy (as policy and as verifier)
- Reduces model collapse compared to always-revise baselines; self-verification outperforms self-consistency as a verifier

## Relevance

PAG completes a three-point design space for generative verifier training alongside RL^V and Tango: RL^V co-trains a verifier for TTS (parallel sampling), Tango co-evolves verifier and generator in interleaved RL, and PAG uses the same model as both policy and verifier with selective revision in a multi-turn loop. The selective revision mechanism is also the natural multi-turn extension of OSPO's ([[2026-07-11-owen-shapley-policy-optimization-a-principled-rl-algorithm-f]]) potential-based reward shaping: PAG's verification step acts as a turn-level signal that determines whether the next turn's compute should be spent on revision.

## My Thoughts

<!-- Add your own notes here -->
