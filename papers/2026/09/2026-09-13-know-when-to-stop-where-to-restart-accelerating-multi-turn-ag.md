---
title: "Know When to Stop, Where to Restart: Accelerating Multi-Turn Agentic On-Policy Distillation"
authors: ["Zhiyu Gui", "Kexin Huang", "Jia Guo", "Junkang Wu", "Zihao Wang", "Zhiqiang Zhang", "Jun Zhou", "Jiancan Wu", "Xiang Wang"]
date: 2026-09-13
arxiv_id: "2609.14636v1"
url: "http://arxiv.org/abs/2609.14636v1"
score: 0.82
topics: [agentic RL, RL training, LLM agent, RLAIF]
status: unread
---

# Know When to Stop, Where to Restart: Accelerating Multi-Turn Agentic On-Policy Distillation (STRIDE)

## Summary

STRIDE identifies two empirical regularities in multi-turn agentic OPD on τ²-bench: informative supervision concentrates in the prefix of each turn, and loss of teacher endorsement is temporally locked to the student's first erroneous action rather than accumulating gradually. Building on these findings, STRIDE combines adaptive early stopping (terminates rollout when cumulative teacher log-probability falls below an OOD threshold) with a prefix buffer (caches high-quality prefixes and restarts at the weakest correct turn), yielding a data-driven curriculum. The method achieves 3.73× speedup while matching full-trajectory OPD and exceeds the 30B teacher on τ²-bench retail; AIME speedups are 5.10× and 3.08×.

## Key Contributions

- Empirical finding: teacher endorsement loss is locked to the student's first erroneous action — not gradual, not random — enabling principled rollout termination rather than budget-based truncation
- Adaptive early stopping: terminates rollout once cumulative teacher log-probability falls below an OOD threshold, directly tracking the structural finding rather than a fixed budget
- Prefix buffer: caches correct prefixes and restarts generation at the weakest correct turn, implementing a data-driven curriculum that progressively extends coverage to later turns
- 3.73× speedup matching full OPD; surpasses 30B teacher on τ²-bench retail; generalizes to AIME (non-agentic) with even higher speedups

## Relevance

STRIDE uses τ²-bench, which also appeared in the Coverage-Not-Targeting paper (Sep 17, V_d ≈ 0.15 as a low verifier-density benchmark). The STRIDE finding that teacher endorsement loss is locked to the first erroneous action provides a complementary perspective: in terminal-state-verified settings, the structural failure point is the first mistake, not the cumulative deviation — consistent with the V_d framework's prediction that coverage (reaching more diverse states) beats targeting (correcting later steps). See also RetireOPD (same day), which addresses the teacher-reliability problem from the architecture side.

## My Thoughts

<!-- Add your own notes here -->
