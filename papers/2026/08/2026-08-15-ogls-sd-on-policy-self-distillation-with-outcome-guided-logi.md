---
title: "OGLS-SD: On-Policy Self-Distillation with Outcome-Guided Logit Steering for LLM Reasoning"
authors: ["Yuxiao Yang", "Xiaoyun Wang", "Weitong Zhang"]
date: 2026-08-15
arxiv_id: "2605.12400"
url: "http://arxiv.org/abs/2605.12400v2"
score: 0.74
topics: [RLAIF, reward model, GRPO, RL training, LLM agent]
status: unread
---

# OGLS-SD: On-Policy Self-Distillation with Outcome-Guided Logit Steering for LLM Reasoning

## Summary

OGLS-SD addresses pattern mismatch in on-policy self-distillation (OPSD) where teacher self-reflection introduces reflection-induced biases that miscalibrate token-level supervision. The solution contrasts teacher logits from successful vs. failed on-policy trajectories to construct an outcome-discriminative steering direction, then steers the teacher logit along this direction before applying KL distillation. This operates at the teacher-logit level rather than the supervision-signal level, distinguishing it from SSOPD's correct/wrong group KL contrast.

## Key Contributions

- Identifies reflection-induced bias in OPSD: self-reflected teacher responses introduce response templates that miscalibrate token-level supervision independent of outcome
- Constructs outcome-discriminative steering direction by contrasting teacher logits from successful vs. failed on-policy trajectories
- Applies steering to modify teacher logit before KL distillation — a "teacher-level" calibration vs. SSOPD's "signal-level" calibration
- Stabilizes self-distillation training and improves over standard OPSD and variants on mathematical reasoning benchmarks

## Relevance

OGLS-SD is the third mechanism in the vault's external-teacher-free supervision taxonomy, alongside SSOPD (outcome-conditioned trajectory contrast) and NOPD (input-corruption contrast). The three mechanisms now form a two-dimensional space: (outcome vs. input perturbation) × (teacher-logit level vs. distillation-signal level). OGLS-SD is outcome-conditioned × teacher-logit level; SSOPD is outcome-conditioned × distillation-signal level; NOPD is input-perturbation × distillation-signal level. The fourth cell (input-perturbation × teacher-logit level) is the unexplored synthesis flagged in the Aug 14 digest. This paper adds a new axis to the NOPD+SSOPD synthesis problem that was queued from Aug 14.

## My Thoughts

<!-- Add your own notes here -->
