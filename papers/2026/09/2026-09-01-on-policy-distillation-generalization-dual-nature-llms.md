---
title: "Every Coin Has Two Sides: On the Dual Nature of Generalization in On-Policy Distillation of Large Language Models"
authors: ["Zhaoyi Li", "Deyang Kong", "Yuan Wei", "Evan Yang", "Ranran Shen", "Mahardika Krisna Ihsani", "Ming Yang", "Wei Zhang", "Chuan Hao", "Jian Yang", "Ran Tao", "Bryan Dai", "Shikun Zhang", "Wei Ye", "Ying Wei", "Defu Lian"]
date: 2026-08-17
arxiv_id: "2608.16647"
url: "https://arxiv.org/abs/2608.16647"
score: 0.81
topics: [RL training, agentic RL, tool use, LLM agent]
status: unread
---

# Every Coin Has Two Sides: On the Dual Nature of Generalization in On-Policy Distillation of Large Language Models

## Summary

A controlled study of on-policy distillation (OPD) generalization systematically varies one factor at a time — in-domain distribution shift, cross-domain transfer, and the multi-teacher setting — finding that OPD transfers a teacher's reasoning behavior rather than its answers to particular problems. Training difficulty barely matters: problems the teacher never solves still provide useful gradient signal. Cross-domain transfer strength depends on the origin relationship between teacher and student domain families, not on dataset size; same-origin pairs bring the student close to the teacher across languages, reasoning horizons, and other domains, while cross-origin pairs mostly fit the trained distribution only.

## Key Contributions

- First controlled OPD generalization study varying one factor at a time (difficulty, domain shift, multi-teacher)
- OPD transfers reasoning behavior, not answer memorization — training difficulty is not a significant factor
- Origin relationship between teacher and student domains predicts cross-domain transfer strength
- Multi-teacher seesaw effect: routing prompts to domain experts cannot confine each teacher's influence; combining teachers creates capability tradeoffs between them
- Practical guidance: OPD is robust to task difficulty selection but sensitive to teacher-student origin alignment

## Relevance

This paper provides the first principled explanation of when OPD generalizes, directly relevant to the AToD/OPDVR comparison thread (Aug 30–31). AToD assumes OPD signal is most useful early in training; OPDVR assumes it varies per-trajectory; this paper shows neither the timing nor trajectory-correctness framing captures the dominant variance — teacher-student origin alignment does. The multi-teacher seesaw effect is also a direct constraint on SAT (Aug 31) and TeamTR (Aug 31): multi-LLM team training inherits the same seesaw if teachers differ in origin.

## My Thoughts

<!-- Add your own notes here -->
