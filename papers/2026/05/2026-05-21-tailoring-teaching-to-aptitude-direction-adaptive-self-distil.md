---
title: "Tailoring Teaching to Aptitude: Direction-Adaptive Self-Distillation for LLM Reasoning"
authors: ["(see arxiv 2605.22263)"]
date: 2026-05-21
arxiv_id: "2605.22263"
url: "https://arxiv.org/abs/2605.22263"
score: 0.86
topics: [RL training, RLHF, RLAIF, OPSD, reward model]
status: unread
---

# Tailoring Teaching to Aptitude: Direction-Adaptive Self-Distillation for LLM Reasoning

## Summary

Proposes DASD, which routes teacher supervision direction by token entropy: high-entropy tokens are pushed away from the privileged teacher (preserving exploration and hypothesis generation), while low-entropy tokens are pulled toward the teacher (stabilizing step-level execution). Identifies uniform teacher imitation across tokens as the root cause of OPSD's failure — it suppresses exploration at high entropy while risking step degradation at low entropy. Achieves best macro Avg@16 across six math benchmarks, with pass@k and reasoning-health analyses confirming that gains come from preserved exploration without sacrificed step accuracy.

## Key Contributions

- Entropy-routed directional supervision: high-entropy → push away (preserve exploration); low-entropy → pull toward (stabilize execution)
- Token-level analysis identifying the two failure modes of uniform teacher imitation (suppress high-entropy exploration, degrade low-entropy accuracy)
- Best macro Avg@16 over strong RLVR and self-distillation baselines on six benchmarks
- Pass@k gains confirm preserved exploration; reasoning-health metrics confirm no step-accuracy trade-off

## Relevance

Directly addresses the core failure mode identified in "Why Does Self-Distillation Degrade" (epistemic verbalization suppression) and "Rethinking OPSD for Thinking Models" (high-entropy forking position suppression — found today). DASD is the most direct mechanistic fix for the exploration-suppression failure, by applying a per-token direction switch rather than global uniform imitation. Extends the OPSD diagnostic cluster with an actionable remedy.

## My Thoughts

<!-- Add your own notes here -->
