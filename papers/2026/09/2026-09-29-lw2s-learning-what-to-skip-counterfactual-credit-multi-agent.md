---
title: "Learning What to Skip: Counterfactual Credit Assignment for Efficient Multi-Agent LLM Workflows"
authors: ["Jinfeng Xu", "Zheyu Chen", "Ziyue Peng", "Zheng Lin", "Shuo Yang", "Jinze Li", "Zheng Xing", "Mengran Li", "Victor C. M. Leung"]
date: 2026-09-29
arxiv_id: "2609.30734v1"
url: "https://arxiv.org/abs/2609.30734"
score: 0.72
topics: [agentic RL, LLM agent, tool use, agentic]
status: unread
---

# Learning What to Skip: Counterfactual Credit Assignment for Efficient Multi-Agent LLM Workflows

## Summary

LW2S formalises component omission in multi-agent LLM workflows as counterfactual credit assignment: controlled skip interventions reveal the per-component marginal contribution, and a safety model learned from those interventions decides which components to skip at runtime. Skip decisions are cascaded (if an early skip is rejected, later components can still be reconsidered), allowing progressive cost-reduction without accuracy loss. Across math reasoning, QA, and code generation, LW2S reduces token cost while matching or improving full-workflow accuracy.

## Key Contributions

- Component-omission framing: multi-agent workflow skip decisions modelled as counterfactual credit assignment over components
- Intervention-derived safety models: skip decisions learned from controlled omission experiments (no manual labels)
- Cascaded skip controller: if early skip is rejected, the controller reconsiders at later stages — avoids binary all-or-nothing commitment
- Token efficiency gains across math, QA, and code benchmarks without accuracy degradation

## Relevance

Tangentially relevant: LW2S applies counterfactual credit reasoning to workflow efficiency rather than RL policy training, so it doesn't directly address the step-credit challenge. The paper is notable as evidence that counterfactual credit has emerged as a unifying principle across the agentic pipeline — from training-time advantage estimation (ASCT, CRR) to runtime workflow optimisation (LW2S). Could inform future RL reward design that penalises unnecessary tool calls or agent steps.

## My Thoughts

<!-- Add your own notes here -->
