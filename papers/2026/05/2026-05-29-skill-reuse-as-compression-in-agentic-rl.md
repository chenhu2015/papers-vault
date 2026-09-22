---
title: "Skill Reuse as Compression in Agentic RL"
authors: ["Zhikun Xu", "Yu Feng", "Jacob Dineen", "Taiwei Shi", "Jieyu Zhao", "Ben Zhou"]
date: 2026-05-29
arxiv_id: "2605.31509v2"
url: "https://arxiv.org/abs/2605.31509"
score: 0.78
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# Skill Reuse as Compression in Agentic RL

## Summary

ReuseRL grounds agentic RL in the Minimum Description Length (MDL) principle, extracting a shared skill dictionary from successful trajectories and augmenting the GRPO objective with a segmentation cost that penalizes idiosyncratic non-compressible behavior. A PAC-Bayes generalization bound links structural compressibility of successful trajectories to out-of-distribution success. Improves both in- and out-of-distribution success over vanilla GRPO and round-length baselines on ALFWorld, TextWorld-Cooking, and Countdown-Stepwise.

## Key Contributions

- MDL-grounded skill extraction: shared skill dictionary built from successful trajectories; segmentation cost penalizes descriptions that encode poorly under the dictionary
- PAC-Bayes bound: formally proves that a dictionary extracted from successful trajectories has bounded expected description length on future successful behavior — principled generalization guarantee
- GRPO augmentation: segmentation cost added directly to RL objective, encouraging structurally compressible policies during training
- Demonstrates that compressibility correlates with generalization across three diverse benchmarks

## Relevance

Provides a theoretical grounding (MDL + PAC-Bayes) for the skill reuse intuition underlying CoSkill and APEx, which are empirically motivated. Together these papers define a spectrum from theory (ReuseRL) to architecture (APEx two-level store) to joint optimization (CoSkill). The MDL framing also connects to ECHO's selective memory — both are asking which trajectory segments are worth retaining, from compression and credit perspectives respectively.

## My Thoughts

<!-- Add your own notes here -->
