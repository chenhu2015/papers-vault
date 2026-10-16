---
title: "RL Post-Training Diffusion Language Models Along Their Own Generation Paths"
authors: ["Vaibhav Singh", "Eugene Belilovsky"]
date: 2026-10-16
arxiv_id: "2610.17266"
url: "https://arxiv.org/abs/2610.17266"
score: 0.80
topics: [reinforcement learning, agentic RL, reward model, PPO]
status: unread
---

# RL Post-Training Diffusion Language Models Along Their Own Generation Paths

## Summary

PACT (Potential-Anchored Consistency of Transitions) extends RL post-training to diffusion language models by learning a scalar potential scoring each intermediate denoising state, anchored by terminal reward. A consistency loss matches the policy-to-reference log-probability ratio to the change in potential, requiring neither sequence-likelihood estimation nor importance-ratio clipping. On four tasks PACT improves LLaDA-8B-Instruct by +9.9 pts on GSM8K, +12.0 on MATH500, +55.7 on Countdown, and +72.6 on Sudoku, reaching the best average accuracy reported for this model class.

## Key Contributions

- Scalar potential function that scores each intermediate denoising state, anchored by terminal reward (reward-tilted reference distribution)
- Consistency loss that matches policy-to-reference log-probability ratio of revealed tokens to the change in potential — avoids sequence-likelihood estimation and importance-ratio clipping
- Extends step-level credit assignment to the non-autoregressive diffusion LM setting
- ~half the training compute of AGRPO to reach the same baseline accuracy on GSM8K

## Relevance

The potential-anchored formulation is a direct analog of value-function-based step credit (compare LVRL from Oct 15), but adapted to diffusion LMs where "steps" are denoising transitions rather than token generations. The "trajectory blindness" problem PACT solves — all denoising steps receiving the same advantage — maps precisely to the token-credit problem motivating OWLET, SPLIT-RL, and ERSR in the autoregressive setting.

## My Thoughts

<!-- Add your own notes here -->
