---
title: "Beyond Teacher Likelihood: Group-Calibrated On-Policy Distillation for Long-Context Reasoning"
authors: ["Zhu Zhang", "Jixun Wang", "Xiaoang Xu", "Xiaorong Wang"]
date: 2026-08-19
arxiv_id: "2608.19181"
url: "https://arxiv.org/abs/2608.19181"
score: 0.81
topics: [RLHF, RLAIF, reward model, RL training]
status: unread
---

# Beyond Teacher Likelihood: Group-Calibrated On-Policy Distillation for Long-Context Reasoning

## Summary

GC-OPD diagnoses and fixes a failure mode of on-policy distillation in long-context tasks: token-level teacher guidance favors locally plausible responses that violate global evidence aggregation, and teacher-verifier alignment degrades monotonically with input length. GC-OPD computes a signed teacher-verifier disagreement residual by separately normalizing verifier rewards and OPD scores within rollout groups, then distributes this residual via Relative-Advantage-based Credit Assignment (RACA). Raises Qwen3-4B from 29.08→40.47 and Qwen3-8B from 35.12→44.65 on five long-context benchmarks.

## Key Contributions

- Diagnoses teacher-verifier disagreement in long-context OPD: alignment degrades monotonically with input length, indicating local-vs-global coherence mismatch
- Group-Calibrated residual: signed disagreement signal from separately normalized verifier rewards and OPD scores within each rollout group
- Relative-Advantage-based Credit Assignment (RACA): distributes trajectory-level residual across tokens by relative OPD advantages while preserving the original OPD signal
- +11 points average on 5 long-context benchmarks over vanilla OPD; open-source at github.com/SolereZhang/GC-OPD

## Relevance

GC-OPD directly extends the OPD thread from Aug 19 ("Towards Understanding On-Policy Distillation" — illusory distillation / sampling efficiency vs. capability). That paper showed OPD gains can be illusory under pass@K analysis; GC-OPD shows a distinct failure mode in long-context settings where the teacher's local token-level guidance conflicts with the verifier's global task evaluation. Together, AlignDistil (theoretical RLHF↔distillation bridge) + GC-OPD (practical calibration fix) + R2-OPD (reasoning progress filtering) form a three-paper cluster addressing complementary OPD failure modes.

## My Thoughts

<!-- Add your own notes here -->
