---
title: "DRACO: Fine-Grained Credit Assignment with Dynamic Rubrics for Long-Horizon Agent Training"
authors: ["Shubham Gandhi", "Saurabh Goyal", "Kiran Kate", "Yara Rizk"]
date: 2026-09-03
arxiv_id: "2609.04094v1"
url: "http://arxiv.org/abs/2609.04094v1"
score: 0.90
topics: [agentic RL, RL training, reward model, GRPO, LLM agent]
status: unread
---

# DRACO: Fine-Grained Credit Assignment with Dynamic Rubrics for Long-Horizon Agent Training

## Summary

DRACO operates in the outcome-blind setting (no programmatic verifier) by generating rubrics dynamically during training to track evolving policy capability, scoring them once per completed trajectory, then redistributing that judgment to responsible steps via closed-form per-step GRPO advantage reweighting — no trained attribution module. Gains 15.9 points over base model and 5.3 over sparse-reward GRPO on AppWorld; generalises out-of-domain to Tau-Bench (+5.3 over base) without a frontier judge.

## Key Contributions

- Dynamic rubric generation during training: rubrics evolve to match the policy's current capability frontier, not fixed human-written criteria
- Closed-form redistribution of trajectory-level rubric scores to per-step GRPO advantages — no additional trained attribution module or verifier
- Strong out-of-domain generalisation: Tau-Bench gains without a frontier judge, despite training on AppWorld
- Works entirely in the outcome-blind setting where ground-truth success signals are unavailable

## Relevance

Extends the credit assignment cluster (GACA, VICT, TRCA, ABSeeker) with a distinct approach: rather than backtracking from known answers or using verifier traces, DRACO uses evolving rubrics as the redistribution signal. The dynamic rubric angle is novel in this cluster and directly relevant to the DRACO-vs-GACA comparison in terms of what attribution signal each method uses.

## My Thoughts

<!-- Add your own notes here -->
