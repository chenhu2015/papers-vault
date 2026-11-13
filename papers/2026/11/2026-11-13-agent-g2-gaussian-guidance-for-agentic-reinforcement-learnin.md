---
title: "Agent-G²: Gaussian Guidance for Agentic Reinforcement Learning"
authors: ["Zixuan Wang", "Yanrui Miao", "Zhengxi Lu", "Teng Pan", "Yiwen Qiu", "Hongxing Li", "Peng Qiu", "Ruiqing Zhang", "Yongliang Shen"]
date: 2026-08-24
arxiv_id: "2608.23318v1"
url: "https://arxiv.org/abs/2608.23318"
score: 0.84
topics: [agentic RL, LLM agent, reinforcement learning, agentic]
status: unread
---

# Agent-G²: Gaussian Guidance for Agentic Reinforcement Learning

## Summary

Agent-G² formalises the depth of hint-based guidance (prefix of an expert trajectory) as a Gaussian whose center and spread are estimated online from rollouts already collected for policy optimisation — no probe rollouts or learned depth predictor required. The center combines a global baseline with per-cluster difficulty; the spread tracks within-cluster variance. Outperforms strongest hint-based, hint-free, and Aux-RL baselines on ALFWorld by 2.3–7.4 points at under one-third the rollout cost of per-sample probing.

## Key Contributions

- Gaussian model of guidance depth: informativeness occupies a band, not a single optimal point
- Online estimation of center (global baseline + per-cluster difficulty) and spread (within-cluster variance) from collected rollouts
- No probe rollouts or learned depth predictor required — reuses rollouts already collected for RL
- Evaluated on ALFWorld and WebShop with Qwen2.5-1.5B/7B-Instruct; consistently outperforms baselines at lower cost

## Relevance

Directly in the adaptive scaffolding cluster (AutoScaffold, JoMoHa, Targeted Guidance) but addresses the specific problem of how much guidance to give per task. The Gaussian band insight is distinct from all three: rather than conditioning on failure (Targeted Guidance) or policy competence (SkillScaffold), it treats guidance depth as a distributional problem with per-cluster heterogeneity.

## My Thoughts

<!-- Add your own notes here -->
