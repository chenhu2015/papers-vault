---
title: "Layer-Isolated Evaluation: Gating the Deterministic Scaffold of a Production LLM Agent with a No-LLM, Regression-Locked Test Harness"
authors: ["Sawyer Zhang", "Alexander Wang", "Sophie Lei"]
date: 2026-08-17
arxiv_id: "2606.11686v1"
url: "http://arxiv.org/abs/2606.11686v1"
score: 0.74
topics: [agentic RL, LLM agent, tool use]
status: unread
---

# Layer-Isolated Evaluation: Gating the Deterministic Scaffold of a Production LLM Agent with a No-LLM, Regression-Locked Test Harness

## Summary

A production LLM ordering agent is decomposed into 7 scaffold layers (ontology, intent, routing, decomposition, escalation, safety, memory), each tested in isolation by a deterministic no-LLM harness; controlled regression injection shows that aggregate task-success masks per-layer failures by 25–91 percentage points while per-slice gates localize faults (injected layer is worst-hit in 5/7 cases, top-3 in 7/7). The coverage-honesty criterion refuses to score any unexercised layer, ensuring evaluation completeness without LLM inference overhead; results replicate across two structurally different tenants (ordering agent and Starbucks SG). This provides a concrete methodology for the Horizon Gap's open problem of decomposing harness/scaffold contributions from model capability.

## Key Contributions

- 7-layer scaffold decomposition for production LLM agents; deterministic, no-LLM per-layer test harness
- Aggregate masking finding: aggregate pass rate drops only 1.7–5.9 pp per injected regression while matching slice craters 25–91 pp
- Coverage-honesty criterion: refuses to score unexercised layers (prevents false "all green" from incomplete coverage)
- Regression injection replication across two structurally different tenants confirms generality

## Relevance

OrchestraBench (today) addresses model-vs-harness at the planning/execution boundary; Layer-Isolated Evaluation addresses it at the scaffold-component level — it shows which layer of the scaffold fails, not just whether the model or harness is responsible. Together they form a two-level decomposition: OrchestraBench separates model from scaffold, Layer-Isolated separates scaffold layers from each other. The aggregate masking finding directly supports the Horizon Gap's critique that outcome-only evaluation obscures long-horizon failure causes, now with controlled empirical evidence from a production system.

## My Thoughts

<!-- Add your own notes here -->
