---
title: "Counterfactual Trace Auditing of LLM Agent Skills"
authors: ["Xiaolin Zhou", "Jinbo Liu", "Li Li", "Ryan A. Rossi", "Xiyang Hu"]
date: 2026-09-04
arxiv_id: "2605.11946v2"
url: "http://arxiv.org/abs/2605.11946v2"
score: 0.77
topics: [LLM agent, agentic RL, tool use, agentic]
status: unread
---

# Counterfactual Trace Auditing of LLM Agent Skills

## Summary

Counterfactual Trace Auditing (CTA) pairs each 'with-skill' agent trace with a 'without-skill' counterpart on the same task, segments both into goal-directed phases, aligns phases, and emits structured Skill Influence Pattern (SIP) annotations — measuring how a skill changes agent behavior rather than just its task outcome. Applied to SWE-Skills-Bench with Claude across 49 tasks, CTA identifies 522 SIP instances despite only a +0.3 pp aggregate pass-rate change, exposing recurring effects invisible to pass rate: literal template copying, off-task artifact creation, excess planning, and task recovery. CTA provides a behavioral measurement lens complementary to CSR's training-level causal consistency: CSR audits whether reasoning steps causally produced the answer; CTA audits whether skill attachment causally changed the behavior.

## Key Contributions

- Counterfactual paired-trace framework: 'with-skill' vs 'without-skill' on the same task, phase-aligned to isolate behavioral attribution
- Skill Influence Pattern (SIP) taxonomy: literal template copying, off-task artifact creation, excess planning, task recovery — four recurring effects pass rate cannot detect
- Pass-rate evaluation gap quantified: 522 behavioral changes detected vs. +0.3 pp aggregate pass-rate — pass rate is near-blind to skill effects on ceiling tasks
- Baseline performance stratification: surface anchoring dominates ceiling tasks; edge-case prompting dominates mid/floor tasks

## Relevance

CTA connects to the Sep faithfulness thread (FACE-Eval, REDAgentBench, CSR) from the evaluation side rather than the training side. FACE-Eval showed CoT is blind to tool returns it acts on; REDAgentBench showed execution violates verbalized constraints; CSR addressed training-level causal consistency. CTA shows that skill attachment itself is behaviorally opaque to pass-rate metrics — the same evaluation gap exists at the skill level as at the reasoning-trace level. Together these papers suggest that standard benchmark metrics systematically undercount misalignment between agent intent, reasoning, and execution.

## My Thoughts

<!-- Add your own notes here -->
