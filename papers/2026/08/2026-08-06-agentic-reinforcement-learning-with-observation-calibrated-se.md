---
title: "Agentic Reinforcement Learning with Observation-Calibrated Self-Distillation"
authors: ["Yi Yang", "Cong Qin", "Xiaodan Liu", "Chishui Chen", "Qing Dong", "Yan Zhang", "Cao Liu", "Zhao Yang", "Lu Pan", "Jiaye Lin", "Yi Feng"]
date: 2026-08-06
arxiv_id: "2608.04788"
url: "https://arxiv.org/abs/2608.04788"
score: 0.92
topics: [agentic RL, RL training, GRPO, LLM agent]
status: unread
---

# Agentic Reinforcement Learning with Observation-Calibrated Self-Distillation

## Summary

OCSD addresses a confounding issue in On-Policy Self-Distillation (OPSD) for agentic RL: the replay scaffold used to derive teacher signals itself perturbs token scores, making it impossible to attribute the support specifically to privileged future observations. OCSD resolves this by contrasting two structurally matched replay views—Full (with future observation) and Observation-Ablated (without)—to isolate an observation residual that discounts scaffold-induced score changes. This residual modulates GRPO updates at high-uncertainty steps while preserving the trajectory-level update direction, consistently outperforming strong baselines on ALFWorld, WebShop, and Search-QA across three Qwen3 model scales.

## Key Contributions

- Identifies scaffold confounding as a failure mode of OPSD: replay views perturb token scores independently of the privileged information they contain
- Proposes observation residual = Full replay score − Observation-Ablated replay score, isolating the observation-specific teacher signal
- Applies the calibrated residual to modulate GRPO updates at high-uncertainty steps while preserving trajectory-level gradient direction
- Diagnostic analysis confirms residual alignment with local environment feedback across ALFWorld, WebShop, Search-QA

## Relevance

OCSD directly advances Gap #19 (ADRS-TVA × PCSD-persistence combined calibration) and Gap #20 (multi-level teacher supervision). Where ADRS uses a confidence-return correlation gate and PCSD uses temporal persistence of teacher advantage, OCSD introduces a third orthogonal calibration axis: contrastive ablation of scaffold-induced score shifts. OCSD is the first paper in the vault to formally decompose the teacher signal into scaffold-induced and observation-induced components, providing a principled separation that ADRS and PCSD do not address.

## My Thoughts

<!-- Add your own notes here -->
