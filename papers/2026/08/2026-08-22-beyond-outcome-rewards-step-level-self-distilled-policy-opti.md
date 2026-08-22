---
title: "Beyond Outcome Rewards: Step-Level Self-Distilled Policy Optimization for Deep Search Agents"
authors: ["Haoze Wu", "Chuqiao Kuang", "Tianyi Zhuang", "Xiaoguang Li"]
date: 2026-08-22
arxiv_id: "2608.12764v1"
url: "https://arxiv.org/abs/2608.12764"
score: 0.87
topics: [agentic RL, GRPO, reward model, tool use, reinforcement learning]
status: unread
---

# Beyond Outcome Rewards: Step-Level Self-Distilled Policy Optimization for Deep Search Agents

## Summary

SSPO addresses the information-asymmetry problem in on-policy self-distillation for search agents: naive OPD lets the teacher (who sees the answer) teach the student the wrong thing, causing it to inherit privileged-information shortcuts rather than better search strategies. The solution is Evidence Anchors — concise web-extracted step-level snippets that give the teacher privileged information without revealing the full answer path — combined with converting teacher-student disagreement into GRPO advantage weights applied only to incorrect trajectories. On Qwen3-8B, SSPO consistently outperforms GRPO across BrowseComp, GAIA, and FRAMES while adding ~5% overhead per step.

## Key Contributions

- **Information-asymmetry diagnosis**: formalises the failure mode of standard OPD applied to search agents — teacher sees the correct answer, student does not, so the teacher's distribution encodes answer leakage rather than better search strategy
- **Evidence Anchors**: step-level privileged snippets extracted from web results that give the teacher signal at the right granularity without answer leakage
- **SSPO training objective**: teacher-student disagreement converted to step-level GRPO advantage weights, applied *only* to incorrect trajectories; correct trajectories are left untouched to preserve diversity
- **Efficiency**: ~5% overhead per step from a single additional forward pass; matches GRPO trained with 2× gradient steps

## Relevance

This paper directly extends the OPD thread that has dominated the vault since Aug 19, addressing the one setting (search agents / tool use) where standard OPD fails for a novel structural reason. It connects the "illusory distillation" finding (Aug 19 OPD paper) and GC-OPD (Aug 21) with the tool-use / agentic RL thread by showing that information asymmetry — not just teacher quality — determines whether OPD provides genuine capability transfer. Evidence Anchors are a design pattern applicable to any agentic setting where the teacher has access to privileged environmental information.

## My Thoughts

<!-- Add your own notes here -->
