---
title: "Credit Without Ground Truth: Auditing Step-Level Credit Assignment in LLM Agents Against Executed Replay"
authors: ["Haiyue Zhang"]
date: 2026-08-20
arxiv_id: "2608.19760"
url: "https://arxiv.org/abs/2608.19760"
score: 0.91
topics: [agentic RL, reward model, LLM agent, RLAIF]
status: unread
---

# Credit Without Ground Truth: Auditing Step-Level Credit Assignment in LLM Agents Against Executed Replay

## Summary

Audited against causal ground truth from executed replay in ALFWorld, none of the standard step-level credit signals (LLM-judge scores, outcome-conditioned logprob ratios, policy confidence) identifies causally important steps better than chance. The study distinguishes step *contribution* (causal, measured by counterfactual replay) from step *correctness* (annotated), finding they systematically diverge: credit signals track the policy's fluency (rank correlation +0.75), not causal impact. A seven-arm training experiment confirms no credit rule outperforms the untrained policy; apparent differences are fully explained by sample size, not credit content.

## Key Contributions

- Causal ground truth via executed replay: re-sampling the policy's own alternatives at each decision point and rolling forward determines step contribution, not correctness
- All common credit signals (LLM-judge, outcome-conditioned logprob, policy confidence) fail to identify causally important steps better than chance
- Causal contribution is sparse (30.5% of decision points carry measurable effect) and model-dependent (counterfactual measurability differs 2× between similar-scale policies)
- Training experiment with seven credit rules: no arm reliably outperforms the untrained policy; differences track sample size (training dose), not credit content

## Relevance

This paper directly challenges the validity of step-level credit assignment signals used throughout the vault's agentic RL training stack — SkillGate (selector credit), RTPO (reverse-tree credit), MileGPO (milestone credit), GUPO (gradient uncertainty). Every paper that uses LLM-judge scores, logprob ratios, or outcome conditioning as credit proxies is subject to this critique: the signals track fluency, not causal contribution. The "Credit Without Ground Truth" finding also extends the vault's distinction between process reward and outcome reward — the implication is that current process reward models may be optimizing for plausibility rather than causal impact.

## My Thoughts

<!-- Add your own notes here -->
