---
title: "Grounded Checklist Partial Credit for Agent Skill Trajectories"
authors: ["Suliu Qin", "Lu Yin", "Xilu Wang"]
date: 2026-09-28
arxiv_id: "2608.27487v1"
url: "https://arxiv.org/abs/2608.27487"
score: 0.72
topics: [agentic RL, LLM agent, tool use]
status: unread
---

# Grounded Checklist Partial Credit for Agent Skill Trajectories

## Summary

GCPC introduces a human-governed, LLM-instantiated partial-credit evaluation framework for agent trajectories: humans define reusable rules once, an LLM instantiates task-specific checklists grounded in the task instruction, and a judge scores each item from execution log evidence alone, abstaining when evidence is missing. Applied to 4,455 SkillsBench trajectories, GCPC achieves AUC 0.689 vs. 0.619 for holistic judging on discriminating PASS/FAIL, and on 1,946 matched pairs exposes 39.6% of trajectories with hidden progress or regression invisible to binary pass@1.

## Key Contributions

- Human-defined reusable rules + LLM task-specific instantiation decouples human labeling effort from per-task scale
- Evidence-grounded scoring: judge abstains when evidence is missing, reducing hallucinated assessments relative to holistic judging
- Exposes 39.6% hidden churn (20.9% improve, 18.7% regress) in matched with/without-skill pairs invisible to binary outcome metrics
- Transfers beyond ALFWorld to Terminal-Bench and SWE-bench

## Relevance

Directly relevant to the evaluation problem surfaced by [[2026-09-28-credit-without-ground-truth-auditing-step-level-credit-assi]]: if step-level credit signals are confounded by dose rather than content, a better partial-credit evaluation framework like GCPC is needed to measure genuine progress. GCPC's checklist-based partial credit could also serve as a better verifier signal for ProCredit-style intermediate rewards, providing richer feedback than binary task success.

## My Thoughts

<!-- Add your own notes here -->
