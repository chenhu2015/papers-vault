---
title: "OrchestraBench: Evaluating Multi-Agent Orchestration Failure Modes, Recovery, and Decomposition Quality"
authors: ["Yidian Chen", "Yingzi Gu", "Natan Vidra", "Spurthi Setty", "Sharon Zheng"]
date: 2026-08-17
arxiv_id: "2608.05263v1"
url: "http://arxiv.org/abs/2608.05263v1"
score: 0.80
topics: [agentic RL, LLM agent, tool use]
status: unread
---

# OrchestraBench: Evaluating Multi-Agent Orchestration Failure Modes, Recovery, and Decomposition Quality

## Summary

OrchestraBench isolates planning quality from execution by standardizing all planners against a cheap Gemini Flash scaffold, revealing that most frontier-model performance differences come from end-to-end system behavior rather than planning capability alone (planner bakeoff p≈0.821, near-equality). The benchmark introduces cascade radius and per-failure-mode recovery as primary metrics across five MAST failure modes, finding that intent-reasoning routers match oracle performance while keyword routers score 0% on adversarial inputs. This directly answers the Horizon Gap's open problem of decomposing model capability from harness/scaffolding contributions with a controlled empirical method.

## Key Contributions

- Scaffold standardization experiment: holds execution fixed (Gemini Flash), varies planner — reveals most prior model-vs-model spread was system-level not capability-level
- Cascade radius metric: quantifies how far a failure propagates in a pipeline (mean 0.9 to 4.7 across depths 3–7)
- Per-failure-mode recovery across 5 MAST modes: tool faults recover fully (1.0), ambiguous delegation partially (0.30), three latent/semantic modes never recover (0.0)
- Trusted-state repair ablation: apparent containment gains come from trusted-state signal, not autonomous detection

## Relevance

The Horizon Gap survey (Aug 16) identified model-vs-harness capability decomposition as a key open problem: existing evaluations conflate what the model contributes with what the scaffolding contributes. OrchestraBench provides a direct empirical methodology — fix the scaffold, vary the model — and finds that much of the apparent capability gap is harness-level, not model-level. The cascade radius metric extends ToolRL-DR's POMDP-component robustness framing (Aug 16) from perturbation sensitivity to failure propagation depth.

## My Thoughts

<!-- Add your own notes here -->
