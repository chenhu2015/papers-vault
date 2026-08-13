---
title: "Reinforcing Step-level Reasoning for Effective Self-Correction in LLMs"
authors: ["Vu Duc Anh", "Nhat M. Hoang", "Do Xuan Long", "Cong-Duy Nguyen", "Ponhvoan Srey", "Luu Anh Tuan"]
date: 2026-08-13
arxiv_id: "2608.11573"
url: "https://arxiv.org/abs/2608.11573"
score: 0.74
topics: [RL training, RLHF, LLM agent, reward model]
status: unread
---

# Reinforcing Step-level Reasoning for Effective Self-Correction in LLMs

## Summary

SFS-DPO is a two-stage RL framework: stage one strengthens step-level reasoning via step-level preference optimization, and stage two explicitly trains self-verification and self-correction capabilities. A teacher-assisted variant (SFS-DPO-R) incorporates explanatory rationales for error verification to provide stronger corrective signals beyond binary preference pairs. Consistent improvements over step-level training baselines across multiple LLMs both in-domain and out-of-domain, with measurable gains in self-correction frequency and effectiveness.

## Key Contributions

- Two-stage separation: step-level reasoning strengthening (stage 1) precedes explicit self-correction training (stage 2) — staged curriculum rather than joint optimization
- Teacher-assisted rationale variant (SFS-DPO-R): incorporates explanatory rationales for verification steps to provide stronger corrective signals
- Generalizes across multiple LLMs in-domain and out-of-domain
- Measurable improvements in both self-correction frequency and correction effectiveness

## Relevance

SFS-DPO's two-stage separation of reasoning quality from correction capability connects to the vault's step-level credit taxonomy: stage 1 uses step-level preference signals (step-level DPO), placing it alongside Guided-OPD and FutureBridge-OPD in the step-level credit mechanism class. The teacher-assisted rationale in SFS-DPO-R is a new form of corrective supervision beyond binary preference pairs, complementing the vault's OPSD/distillation thread where teacher corrections are decomposed at the token level. The self-verification training in stage 2 parallels the vault's verifiable process supervision thread from Aug 11 (VPS paper that missed the top-5 cap), providing empirical evidence that explicitly training verification is more effective than relying on implicit reasoning improvements.

## My Thoughts

<!-- Add your own notes here -->
