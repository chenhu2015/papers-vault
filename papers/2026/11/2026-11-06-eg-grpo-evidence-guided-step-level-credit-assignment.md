---
title: "EG-GRPO: Evidence-Guided Step-level Credit Assignment for Deep Search Agents"
authors: ["Sijia Luo", "Mengjie Gao", "Yuxiao He", "Mengshu Sun", "Cuiping Li", "Hong Chen", "Jing Zhang"]
date: 2026-10-18
arxiv_id: "2610.25269v1"
url: "http://arxiv.org/abs/2610.25269v1"
score: 0.83
topics: [agentic RL, GRPO, RL training, LLM agent, tool use]
status: unread
---

# EG-GRPO: Evidence-Guided Step-level Credit Assignment for Deep Search Agents

## Summary

EG-GRPO constructs step-level process rewards for deep search agents by identifying the first supporting citation for each required evidence claim in synthetic search data, using the incrementally acquired evidence as a state-conditioned knowledge state for relative advantage estimation. This evidence-grounded step signal is combined with the standard trajectory-level GRPO advantage, providing explicit supervision for the information-gathering phase of search rather than rewarding only the final answer. Across five challenging deep search benchmarks and multiple model scales, EG-GRPO generally outperforms standard GRPO and existing reward-enhanced and step-level RL baselines.

## Key Contributions

- Evidence-grounded step rewards: first citation for each claim defines the rewarded step
- Evolving knowledge state enables state-conditioned relative advantage estimation per step
- Combined step + trajectory signal consistently outperforms outcome-only and existing process reward methods
- Generalizes across deep search benchmarks and model scales without requiring additional annotation beyond synthetic data

## Relevance

Pairs directly with GCA (Nov 6, also focused on search agent credit assignment) and EG-GRPO complements it from the annotation side: where GCA corrects credit post-hoc using verifiable sub-outcomes, EG-GRPO uses explicit evidence annotations to build step rewards prospectively. Both papers suggest that the key failure mode in search agent RL is insufficient credit for the retrieval phase — a finding that motivates rethinking agentic RL data pipelines to include evidence annotations.

## My Thoughts

<!-- Add your own notes here -->
