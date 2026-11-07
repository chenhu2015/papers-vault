---
title: "CREDO: Evidence-Conditioned Credit Assignment for Temporal Reasoning Agents"
authors: ["Yue Leng", "Shengtao Wen", "Xiang Chen", "Xinyi Zeng", "Yu Tian", "Sheng-Jun Huang"]
date: 2026-11-01
arxiv_id: "2611.01643v1"
url: "https://arxiv.org/abs/2611.01643"
score: 0.82
topics: [agentic RL, GRPO, reinforcement learning, LLM agent, RLHF, RLAIF]
status: unread
---

# CREDO: Evidence-Conditioned Credit Assignment for Temporal Reasoning Agents

## Summary

CREDO addresses the GRPO limitation that trajectory-level outcome signals cannot distinguish intermediate decision quality: downstream failures penalize useful evidence acquisition, and all-failed groups eliminate relative signal despite differing intermediate progress. It uses intermediate evidence to recover local supervision in all-failed groups and uses retained answer overlap as an opportunity proxy to redistribute part of the outcome-policy weight toward the reasoning and answering stages. Applied to Temporal Knowledge Graph QA, CREDO raises Overall accuracy from 78.0% to 82.4% on MultiTQ and cross-KG accuracy from 30.9% to 36.4% on TimelineKGQA.

## Key Contributions

- Recovers local supervision in all-failed GRPO groups using intermediate evidence, eliminating the zero-signal all-failed problem
- Opportunity proxy: retained answer overlap between evidence and answer steps used to shift outcome-policy weight toward reasoning/answering
- Credit redistribution preserves terminal rewards and trajectory-level advantages while reallocating weight locally
- Strong gains on temporal KG QA: +4.4% Overall on MultiTQ, +10.6% Multiple, +5.5% cross-KG on TimelineKGQA

## Relevance

CREDO is a new step-credit cluster member specifically motivated by the all-failed-group failure mode (zero relative signal) — a problem also touched on by Direction-Aware Token Credit Assignment (DATC) and C3. The evidence-overlap proxy for opportunity is closely related to EG-GRPO's evidence-citation annotations but applied to temporal reasoning agents rather than deep search.

## My Thoughts

<!-- Add your own notes here -->
