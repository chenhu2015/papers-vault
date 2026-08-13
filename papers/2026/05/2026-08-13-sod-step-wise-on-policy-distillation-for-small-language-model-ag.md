---
title: "SOD: Step-wise On-Policy Distillation for Small Language Model Agents"
authors: ["Qiyong Zhong", "Mao Zheng", "Mingyang Song", "Xin Lin", "Jie Sun", "Houcheng Jiang", "Xiang Wang", "Junfeng Fang"]
date: 2026-08-13
arxiv_id: "2605.07725"
url: "https://arxiv.org/abs/2605.07725"
score: 0.78
topics: [agentic RL, tool use, RL training, LLM agent, GRPO]
status: unread
---

# SOD: Step-wise On-Policy Distillation for Small Language Model Agents

## Summary

SOD identifies a cascading-error failure mode of OPD applied to tool-integrated reasoning: erroneous tool calls propagate across steps, causing progressive student-teacher divergence that makes token-level supervision increasingly unreliable in high-divergence regions. SOD adaptively reweights distillation strength per step based on step-level divergence, attenuating misleading signals where divergence is high while preserving dense guidance in well-aligned states. A 0.6B student trained with SOD achieves 26.13% on AIME 2025 and up to 20.86% improvement over the second-best baseline across math, science, and code benchmarks.

## Key Contributions

- Identifies cascading-error failure mode: erroneous tool calls at step T amplify student-teacher divergence at steps T+1, T+2, ..., making token-level supervision progressively unreliable
- Step-level divergence-adaptive distillation weight: attenuates signals in high-divergence regions, preserves guidance in well-aligned states
- Effective distillation to 0.6B model achieving 26.13% on AIME 2025 — demonstrates agentic reasoning transfer to lightweight models
- Up to 20.86% improvement over second-best baseline across math, science, and code benchmarks

## Relevance

SOD's divergence-adaptive step weighting connects directly to the vault's credit calibration taxonomy (Gap #19's axis D: DASH sequential divergence history). DASH uses within-rollout divergence sequences to calibrate token-level credit; SOD uses step-level divergence to calibrate distillation strength — both gate supervision based on divergence, but DASH is a diagnostic axis for credit calibration and SOD is a training-time intervention. SOD also directly addresses the vault's agentic RL thread: the cascading-error failure mode is unique to multi-step tool-integrated reasoning (where tool calls have permanent state effects) and is absent in single-step reasoning RL. This is a new failure mode category orthogonal to the vault's existing all-fail/all-correct problem and the credit surface-concentration finding (CSCR).

## My Thoughts

<!-- Add your own notes here -->
