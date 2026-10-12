---
title: "Residual Visual Credit Optimization: Conserved Evidence Routing for Multimodal Reinforcement Learning"
authors: ["Lin Qiu", "Yao Liu", "Diyi Hu", "Hanqing Zeng", "Onur Gungor", "Chujie Chen", "Jiayi Liu", "Jianyu Wang", "XueLin Zheng"]
date: 2026-10-04
arxiv_id: "2610.04918v1"
url: "http://arxiv.org/abs/2610.04918v1"
score: 0.90
topics: [VLM, multimodal, vision-language, agentic RL, RL training, GRPO, reward model]
status: unread
---

# Residual Visual Credit Optimization: Conserved Evidence Routing for Multimodal Reinforcement Learning

## Summary

RVCO treats per-token credit in multimodal RL as a conserved routing problem: a controlled visual intervention yields per-token evidence response, and a budgeted entropic router distributes a fixed amount of sequence utility according to perceptual dependence. The resulting credit field is selective, bounded, full-support, and invariant to response-local score shifts, recovering hard token selection as a limiting case. Across four model families and seven reasoning benchmarks, RVCO improves over RLVR baselines while leaving rewards, rollouts, and the group-relative advantage estimator unchanged — only the geometry of token-level credit differs.

## Key Contributions

- Frames token credit as a conserved quantity: the entropic router redistributes a fixed total credit budget rather than scaling it arbitrarily
- Controlled visual intervention + within-trajectory coordinate normalization produces a per-token perceptual dependence signal robust to scale
- Residual support path guarantees positive credit at every valid position; analytic correction restores prescribed credit mass exactly
- Plug-in: rewards, rollouts, and GRPO advantage estimator are untouched — only the credit geometry changes

## Relevance

Directly extends the VLM RL credit assignment thread (TPAE, persistence-aware, TTRSD, TTIQ, SAVOR, DyCPO) with a conservation-law framing that is new to this cluster. The "budget-constrained entropic router" angle is adjacent to DyCPO's co-evolution approach but formalizes the credit field differently — worth comparing whether conservation constraints improve stability over DyCPO's dynamic self-diagnosis.

## My Thoughts

<!-- Add your own notes here -->
