---
title: "Model or Harness? An Interaction-Centric Taxonomy for Localizing Agent Failures"
authors: ["Harsh Raj", "Vipul Gupta", "Anas Mahmoud", "Razvan-Gabriel Dumitru"]
date: 2026-08-18
arxiv_id: "2607.28802"
url: "http://arxiv.org/abs/2607.28802v1"
score: 0.81
topics: [agentic RL, LLM agent, agentic evaluation, tool use]
status: unread
---

# Model or Harness? An Interaction-Centric Taxonomy for Localizing Agent Failures

## Summary

The paper introduces a 41-failure-mode interaction-centric taxonomy that assigns each failure to an edge between two agent components (model, harness, user, tool, memory, environment) and a fault side indicating where the repair belongs. This makes the taxonomy directly actionable: model-side failures target post-training, harness-side failures target scaffolding fixes, and environment failures point to evaluation redesign. Reproducibility is validated via LLM judges across four frontier models reaching Cohen's κ=0.76 against human labels.

## Key Contributions

- 41-failure-mode taxonomy organised by interaction edge and fault side, covering coding assistants through long-horizon personal assistants and multi-agent systems
- Actionable repair assignment: each failure mode points to a specific intervention class (post-training, harness engineering, environment/grader redesign)
- LLM-judge reproducibility evaluation: Cohen's κ=0.76 across four frontier models, indicating shared categorical structure rather than annotator-specific labels
- Grounds taxonomy in public benchmark cases, model system cards, published reports, and logged trajectories

## Relevance

This paper directly resolves the model-vs-harness open problem identified in the Aug 17 digest (surfaced by OrchestraBench). OrchestraBench empirically showed that most frontier-model performance differences are system-level (p≈0.821); "Model or Harness?" provides the structural vocabulary and 41-mode taxonomy for assigning any specific failure to a component interaction edge. Together with LongRCA Bench (Aug 18), this completes a three-level failure attribution stack: taxonomy → cascade → root-step.

## My Thoughts

<!-- Add your own notes here -->
