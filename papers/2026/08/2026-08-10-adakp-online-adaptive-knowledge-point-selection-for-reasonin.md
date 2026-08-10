---
title: "AdaKP: Online Adaptive Knowledge-Point Selection for Reasoning-Oriented Reinforcement Learning"
authors: ["Zibin Meng", "Zhenyu Zhao", "Chunqiang Run"]
date: 2026-08-10
arxiv_id: "2607.24833"
url: "https://arxiv.org/abs/2607.24833"
score: 0.73
topics: [GRPO, RLAIF, agentic]
status: unread
---

# AdaKP: Online Adaptive Knowledge-Point Selection for Reasoning-Oriented Reinforcement Learning

## Summary

AdaKP introduces online adaptive selection of atomic knowledge point (KP) hints for RL training with verifiable rewards, addressing reward sparsity on competition-level mathematics via DAPO+GRPO. An entropy-reduction proxy evaluates each KP by the decrease in next-token entropy it induces in a single forward pass (provably bounded truncation bias), with momentum smoothing, retirement-revival, and front-loaded revaluation scheduling for stable online selection. A pre-flight validation gate certifies the proxy against leave-one-out ground truth before training, improving over a static-selection baseline on all eight competition-math benchmarks at negligible cost.

## Key Contributions

- Entropy-reduction proxy for KP evaluation: scores a KP by the decrease in next-token entropy it induces, replacing expensive rollout-based estimation with a single forward pass
- Three online stability mechanisms: momentum smoother (absorbs per-step noise), retirement-revival manager (prunes weak KPs while preserving exploration), adaptive scheduler (front-loads re-evaluations into early training)
- Pre-flight validation gate certifying entropy proxy against leave-one-out ground truth before expensive runs, converting method-level risk into a falsifiable check
- Fully additive fork of DAPO+GRPO — no optimizer changes required

## Relevance

AdaKP introduces prompt-level online curriculum selection as a new axis in the vault's RL training paradigm space. The entropy-reduction proxy for hint selection is analogous to the ability-aware environment selection in AES-HDC (quality > quantity for environment selection) but operates at the knowledge-hint injection level in GRPO training. The retirement-revival mechanism also parallels GRPO's all-fail filtering thread (Gap #16): where MMPO and Dark Room handle groups where all rollouts fail, AdaKP's retirement-revival handles KPs that consistently fail to improve rollouts.

## My Thoughts

<!-- Add your own notes here -->
