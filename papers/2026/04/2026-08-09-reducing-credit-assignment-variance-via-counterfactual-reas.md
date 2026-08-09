---
title: "Reducing Credit Assignment Variance via Counterfactual Reasoning Paths"
authors: ["Fei Ding", "Yongkang Zhang", "Youwei Wang", "Zijian Zeng"]
date: 2026-08-09
arxiv_id: "2605.16302"
url: "https://arxiv.org/abs/2605.16302"
score: 0.75
topics: [GRPO, reward model, RL training, agentic RL, RLHF]
status: unread
---

# Reducing Credit Assignment Variance via Counterfactual Reasoning Paths

## Summary

IBPO samples multiple reasoning trajectories per input and uses their differences as implicit process-level advantage estimators, converting sparse terminal rewards into step-sensitive learning signals that reduce gradient variance. This counterfactual-comparison framework substantially improves training stability and the performance ceiling on math and code reasoning benchmarks over GRPO baselines.

## Key Contributions

- Counterfactual-comparison framework: treats differences between simultaneously-sampled trajectories as implicit counterfactuals for intermediate decision quality
- Implicit process-level advantage: step-sensitive advantage estimator derived from trajectory divergence, without requiring explicit process reward models or teacher models
- IBPO algorithm: builds on the framework to improve training stability and reduce gradient variance from sparse terminal rewards
- Demonstrated improvements on mathematical and code reasoning benchmarks

## Relevance

IBPO extends the vault's credit assignment taxonomy by introducing a **multi-trajectory implicit credit** approach that sits between GRPO's uniform broadcast and OPSD's explicit teacher distillation. Unlike Parallel Shapley (Aug 6, 0.78) which uses cooperative game theory to assign credit to parallel paths, IBPO uses trajectory differences as implicit counterfactuals — no explicit attribution model is required. Unlike OPSD/CSCR which require a privileged teacher, IBPO derives process-level signal entirely from within-batch trajectory diversity. This is structurally closer to how RAPO uses retrieved trajectories as exploration signals, but applied at the within-batch level and for credit (not exploration) purposes.

## My Thoughts

<!-- Add your own notes here -->
