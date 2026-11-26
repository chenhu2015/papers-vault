---
title: "Are We Rewarding the Wrong Module? Module-Specific Policy Optimization for Multimodal Reinforcement Learning"
authors: ["HuiSeong Cho", "Jun Yeong Park", "Yu Rang Park"]
date: 2026-11-24
arxiv_id: "2611.32687"
url: "https://arxiv.org/abs/2611.32687"
score: 0.85
topics: [RLVR, GRPO, multimodal models, VLM, reward model]
status: unread
---

# Are We Rewarding the Wrong Module? Module-Specific Policy Optimization for Multimodal Reinforcement Learning

## Summary

MSPO diagnoses Module-Level Credit Entanglement in GRPO, where the vision encoder, projector, and LLM are jointly updated with the same advantage even when perceptual and answer correctness diverge. It introduces a Confidence-aware Perception Reward (CaPR) derived from perception checklists to guide vision encoder updates separately, while the projector and LLM retain standard GRPO. Outperforms existing RL-tuned MLLMs on 7 reasoning benchmarks at 3B and 7B scale.

## Key Contributions

- Identifies Module-Level Credit Entanglement as a systematic GRPO failure mode: same advantage signal applied to vision encoder, projector, and LLM regardless of their different correctness contributions
- Proposes Confidence-aware Perception Reward (CaPR): perception checklists generate auxiliary perception accuracy, thresholded to a sign; posterior confidence from a Beta distribution scales reward magnitude
- Derives vision encoder advantage via group-relative normalization of CaPR scaled by main-task success rate, decoupled from the projector/LLM GRPO updates
- Outperforms GRPO baselines on 7 mathematical and general reasoning benchmarks at both 3B and 7B scale

## Relevance

Directly advances the RLVR training stability thread — specifically the question of how to fix credit assignment failures in GRPO for MLLMs that have distinct vision and language modules. Extends the tool-token credit assignment work (TACA) from the agentic domain into the multimodal reasoning domain: the core insight that uniform advantage across unlike modules distorts training is now confirmed across two independent papers.

## My Thoughts

<!-- Add your own notes here -->
