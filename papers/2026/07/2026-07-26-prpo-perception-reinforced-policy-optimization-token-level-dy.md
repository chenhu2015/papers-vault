---
title: "PRPO: Perception-Reinforced Policy Optimization via Token-Level Dynamic Advantage Reshaping"
authors: ["Qiming Li", "Tianlun Li", "Xiaolong Cheng", "Hangyu Li", "Ruiyan Gong", "Kangning Niu", "Kaitao Jiang", "Mu Xu"]
date: 2026-07-26
arxiv_id: "2606.08708"
url: "https://arxiv.org/abs/2606.08708"
score: 0.88
topics: [multimodal models, vision language models, VLM, agentic RL, GRPO, reward model]
status: unread
---

# PRPO: Perception-Reinforced Policy Optimization via Token-Level Dynamic Advantage Reshaping

## Summary

Addresses the mismatch between trajectory-level RLVR and multimodal reasoning, where only a sparse subset of tokens is causally grounded in visual evidence — pivotal perceptual tokens receive the same gradient signal as filler and template tokens under standard GRPO. Introduces Robust Visual Dependency (RVD), a metric identifying tokens that are both visually grounded and perturbation-stable, and Perceptual Advantage Reshaping (PAR), which amplifies advantage on those pivotal tokens while preserving stable gradients elsewhere. Achieves average gains of 23.3% and 21.1% across seven multimodal benchmarks at 3B and 7B scale respectively.

## Key Contributions

- Robust Visual Dependency (RVD): measures which tokens are both visually grounded (causally linked to visual input) and perturbation-stable (not brittle to image noise)
- Perceptual Advantage Reshaping (PAR): token-level credit reshaping that amplifies advantage on high-RVD tokens and dampens it on non-perceptual tokens
- Validated at both 3B and 7B scales; improved training efficiency and stronger cross-task generalization vs. standard GRPO-based LVLM training
- Addresses the long-confirmed Gap #4 (dedicated VLM credit assignment / reward signal design) from a novel perceptual-grounding angle

## Relevance

PRPO bridges two persistent open threads: token-level credit assignment (previously studied by OPPO, GRAIL, TACO for LLMs) and multimodal RL (previously studied by APO, DyCo-RL, SIVA-RL for VLMs). RVD is a structurally novel signal: unlike gradient saliency (GRAIL), OT (HPO), or Bayesian recursion (OPPO), it measures visual causal grounding specifically — a property unique to the multimodal setting. This is the most principled VLM-specific token-level credit assignment paper in the vault.

## My Thoughts

<!-- Add your own notes here -->
