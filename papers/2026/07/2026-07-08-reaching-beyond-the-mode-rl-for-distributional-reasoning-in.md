---
title: "Reaching Beyond the Mode: RL for Distributional Reasoning in Language Models"
authors: ["Anonymous"]
date: 2026-07-08
arxiv_id: "2603.24844v1"
url: "https://arxiv.org/abs/2603.24844"
score: 0.75
topics: [RL training, RLHF, RLAIF, agentic RL, reward model]
status: unread
---

# Reaching Beyond the Mode: RL for Distributional Reasoning in Language Models

## Summary

Frames post-training mode collapse — where standard RL/RLHF collapses the model's implicit answer distribution onto a single dominant mode — as the core failure in tasks requiring multiple valid answers (medical diagnosis, ambiguous QA, incomplete-information settings), and proposes multi-answer RL that modifies the RL objective so models generate multiple candidate answers with confidence estimates in a single forward pass. Achieves improved diversity, coverage, and set-level calibration across QA, medical diagnosis, and coding benchmarks, requiring fewer tokens than repeated sampling; positions multi-answer RL as a compute-efficient alternative to inference-time scaling procedures such as best-of-k.

## Key Contributions

- Frames answer-distribution collapse as a post-training RL failure mode distinct from behavioral (TA-GRPO) or capability (RL-PLUS) collapse — this is semantic/distributional collapse at the output level
- Multi-answer RL objective: modifies the RL reward to credit coverage over the set of valid answers, not just the best single answer, internalizing best-of-k search into the model's generative process
- Improves set-level calibration (models know which answers they are uncertain about) alongside diversity
- Coding tasks show substantially improved accuracy alongside diversity; demonstrates multi-answer RL generalizes beyond open-ended QA

## Relevance

This paper adds a sixth candidate failure mode to the RLVR taxonomy in the vault: answer-distribution collapse, distinct from the five named failure modes (SeL, diversity/gradient collapse, capability boundary collapse, view-dependent advantage collapse, rise-and-collapse). The multi-answer RL objective is structurally complementary to TA-GRPO's (Jul 6) group-level rephrasing: TA-GRPO diversifies the *input* distribution to prevent gradient vanishing, while multi-answer RL diversifies the *output target* distribution to prevent distributional collapse. Together they represent input- and output-side diversity interventions for RLVR, and combining them is a natural next experiment.

## My Thoughts

<!-- Add your own notes here -->
