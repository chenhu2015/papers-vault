---
title: "Team-Based Self-Play With Dual Adaptive Weighting for Fine-Tuning LLMs"
authors: ["Wu Li", "Yigeng Zhou", "Zesheng Shi", "Yequan Wang", "Min Zhang", "Jing Li"]
date: 2026-09-06
arxiv_id: "2605.09922"
url: "https://arxiv.org/abs/2605.09922"
score: 0.78
topics: [RLHF, RLAIF, reinforcement learning, RL training, LLM agent, agentic RL]
status: unread
---

# Team-Based Self-Play With Dual Adaptive Weighting for Fine-Tuning LLMs

## Summary

TPAW frames LLM fine-tuning as a team competition between the current policy and a pool of historical checkpoints, with two adaptive weighting mechanisms: response reweighting adjusting target-response importance by estimated difficulty, and player weighting modulating each checkpoint's contribution during training. Initialized from SFT, TPAW iteratively refines alignment without human supervision, consistently outperforming self-training baselines across models and benchmarks. TPAW advances the Agon generalization thread by demonstrating that rival-grading dynamics (current vs. historical pool) combined with adaptive weighting can drive stable self-supervised improvement across general alignment tasks beyond math/code.

## Key Contributions

- Team-based self-play: current policy collaborates with and competes against historical checkpoints, providing curriculum-like pressure without explicit curriculum design
- Response reweighting: adjusts importance of target responses by estimated difficulty (addresses the diminishing-gap problem in iterative self-training)
- Player weighting: dynamically modulates each historical team member's contribution to prevent instability and bias amplification
- No external supervision or teacher-student hierarchy required — purely self-supervised from SFT initialization

## Relevance

TPAW is the closest paper to Agon's rival-grading dynamic yet found after three search attempts. Key structural difference: Agon uses a live rival model grading the current model's outputs simultaneously; TPAW uses competition against historical checkpoints. The dual adaptive weighting (response + player) addresses two failure modes that Agon does not explicitly handle — the diminishing-gap problem (positive/negative responses converge over iterations) and instability from low-quality historical checkpoints. TPAW's breadth (general alignment across diverse LLM benchmarks) directly addresses the Agon generalization gap (Agon demonstrated only on math). The historical-checkpoint team mechanism also connects to Demystifying RL Post-Training's base-model-prior finding: historical checkpoints encode prior-training distributions, and player weighting effectively calibrates how much each prior contributes to the training signal.

## My Thoughts

<!-- Add your own notes here -->
