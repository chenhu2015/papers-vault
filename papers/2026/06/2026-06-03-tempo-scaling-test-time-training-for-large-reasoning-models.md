---
title: "TEMPO: Scaling Test-time Training for Large Reasoning Models"
authors: ["Qingyang Zhang", "Xinke Kong", "Haitao Wu", "Qinghua Hu", "Minghao Wu", "Baosong Yang", "Yu Cheng", "Yun Luo", "Ganqu Cui", "Changqing Zhang"]
date: 2026-06-03
arxiv_id: "2604.19295"
url: "https://arxiv.org/abs/2604.19295"
score: 0.75
topics: [RL training, reinforcement learning, RLHF, reward model, LLM agent, agentic RL]
status: unread
---

# TEMPO: Scaling Test-time Training for Large Reasoning Models

## Summary

TEMPO identifies that test-time training for LLMs plateaus because self-generated reward signals drift as the policy evolves — prior methods omit the crucial critic recalibration step. Formalizing TTT as EM, TEMPO interleaves policy refinement (E-step) with periodic recalibration on a labeled dataset (M-step), tightening the ELBO and sustaining improvement. Results: OLMO3-7B improves from 33.0% to 51.1% on AIME 2024; Qwen3-14B from 42.3% to 65.8%.

## Key Contributions

- EM formalization of test-time training shows prior TTT methods are incomplete E-step-only variants, explaining why they plateau
- Periodic critic recalibration on a small labeled set prevents reward signal drift as the policy evolves
- Maintains output diversity (prevents collapse) through the M-step recalibration constraint
- Strong results across Qwen3 and OLMO3 families: +18.1% absolute AIME improvement for OLMO3-7B

## Relevance

Bridges the RL training and test-time compute threads: TEMPO uses RL-style policy refinement at inference, addressing the same reward drift problem discussed in the reward hacking/OOD thread (Reward Bias Substitution, May 31). The EM perspective offers a clean theoretical lens for understanding when self-supervised RL signals fail.

## My Thoughts

<!-- Add your own notes here -->
