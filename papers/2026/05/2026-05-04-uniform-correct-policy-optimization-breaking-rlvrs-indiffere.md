---
title: "Uniform-Correct Policy Optimization: Breaking RLVR's Indifference to Diversity"
authors: ["Anamika Lochab", "Bolian Li", "Ruqi Zhang"]
date: 2026-05-01
arxiv_id: "2605.00365v1"
url: "http://arxiv.org/abs/2605.00365v1"
score: 0.82
topics: [GRPO, agentic RL, RL training, RLHF]
status: unread
---

# Uniform-Correct Policy Optimization: Breaking RLVR's Indifference to Diversity

## Summary

UCPO formally characterises GRPO's diversity collapse: the objective's indifference to how probability mass distributes among correct solutions causes a self-reinforcing concentration on a narrow subset of outputs. The authors prove the Uniform-Correct Policy is uniquely optimal under both robustness and entropy-regularised criteria, and propose a conditional uniformity penalty on correct-solution distributions. Across 1.5B–7B models on five mathematical reasoning benchmarks, UCPO improves Pass@K by up to +10% absolute on AIME24 while maintaining competitive Pass@1.

## Key Contributions

- Formally proves GRPO's indifference to correct-solution distribution causes self-reinforcing diversity collapse (not just empirically observed)
- Characterises the Uniform-Correct Policy as uniquely optimal under both robustness and entropy-regularised criteria
- Adds a conditional uniformity penalty to GRPO that redistributes gradient signal toward underrepresented correct responses
- +10% absolute Pass@64 on AIME24; up to 45% higher equation-level diversity within the correct set

## Relevance

GRPO is one of the core profile keywords and has appeared across the vault (Oracle-RLAIF used GRPO_rank, MM-Doc-R1 fixed GRPO baseline bias). UCPO provides the first formal characterisation of *why* GRPO collapses, complementing the SAE paper's analysis of biased advantage estimation — both identify structural failure modes in standard GRPO training that require architectural fixes rather than hyperparameter tuning.

## My Thoughts

<!-- Add your own notes here -->
