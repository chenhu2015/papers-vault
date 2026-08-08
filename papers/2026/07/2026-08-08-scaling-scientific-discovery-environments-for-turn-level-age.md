---
title: "Scaling Scientific Discovery Environments for Turn-Level Agentic RL"
authors: ["Yucheng Xu", "Keyi Zhang", "Yuyang Yu", "Min Zhang", "Shiyuan Meng", "Pei Chu", "Zhongying Tu"]
date: 2026-08-08
arxiv_id: "2607.28990v1"
url: "http://arxiv.org/abs/2607.28990v1"
score: 0.71
topics: [agentic RL, LLM agent, RL training]
status: unread
---

# Scaling Scientific Discovery Environments for Turn-Level Agentic RL

## Summary

SciDisco introduces a scalable framework for training scientific discovery LLM agents in process-verifiable environments: SciThèque compiles hypotheses, datasets, hidden evidence graphs, and verifiers into task environments checkable mid-interaction, while DAG-grounded trajectory synthesis constructs verifier-filtered multi-turn demonstrations. DiscoPO assigns turn-level credit to actions that produce verifiable analytical evidence, and SciDisco-14B achieves state-of-the-art on hypothesis-driven scientific data analysis benchmarks.

## Key Contributions

- SciThèque: process-verifiable environment compilation for scientific discovery with mid-interaction progress checks
- DAG-grounded trajectory synthesis using environment verifiers for demonstration filtering
- DiscoPO: turn-level credit assignment from verifiable analytical evidence production
- SciDisco-14B achieves state-of-the-art on hypothesis-driven scientific data analysis

## Relevance

SciDisco's DiscoPO is relevant to the turn-level credit assignment thread in the vault: where FutureBridge-OPD selects high-disagreement states via future trajectory simulation for privileged distillation, DiscoPO assigns per-turn credit based on verifiable evidence production in a scientific analysis context. The verification-grounded credit signal is structurally different from divergence-based calibration (DASH/PCSD/ADRS/OCSD) — it's outcome-grounded (did this turn produce analytically verifiable evidence?) rather than distributional. The DAG-grounded trajectory synthesis also connects to the EnvFactory approach of constructing grounded training trajectories.

## My Thoughts

<!-- Add your own notes here -->
