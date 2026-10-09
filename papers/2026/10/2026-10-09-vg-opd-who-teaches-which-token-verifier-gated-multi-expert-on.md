---
title: "Who Teaches Which Token? Verifier-Gated Multi-Expert On-Policy Distillation for Scientific Reasoning"
authors: ["Xun Xu", "Zaixi Zhang"]
date: 2026-09-14
arxiv_id: "2609.15404"
url: "https://arxiv.org/abs/2609.15404"
score: 0.85
topics: [GRPO, agentic RL, RL training, reward model, RLAIF]
status: unread
---

# Who Teaches Which Token? Verifier-Gated Multi-Expert On-Policy Distillation for Scientific Reasoning

## Summary

VG-OPD licenses expert teachers to supervise specific tokens by verifying their counterfactual gain on particular answer criteria, converting this into a gated KL divergence term that enters GRPO as an additive token-level advantage. Token-level supervision is gated by criterion satisfaction, so supervision is concentrated only where an expert is verified useful — misplacing the same supervision budget to wrong tokens is shown to be the single most damaging ablation, even dragging performance below RL solo. Evaluated across seven benchmarks at 4B and 8B scales, VG-OPD ranks first on five.

## Key Contributions

- Verifier-gated token supervision: criterion-satisfaction check licenses a teacher expert at a specific token; disagreement between expert and student localises the supervision target
- Gated KL as GRPO advantage: the verified KL divergence enters the GRPO objective as an additive token-level advantage (not just a loss term), directly modifying credit assignment
- Multi-expert capability domains: different RL-trained experts for different knowledge domains; criterion importance sets inter-expert weighting
- Key ablation: misplacing verified supervision (correct budget, wrong token) is more damaging than removing all distillation — locality of credit is the mechanism, not quantity

## Relevance

This is a direct extension of the BoT-GRPO thread (Oct 8). BoT-GRPO uses a token-level PRM to enrich GRPO; VG-OPD uses a verifier-gated teacher KL to inject token-level advantage into GRPO from a different source. Together they converge on the same principle: token-level credit placement in GRPO is the mechanism, whether the signal comes from a process reward model or a verifier-gated distillation. The finding that misplaced supervision degrades below RL solo directly answers the BoT-GRPO open question about what happens when the token-level RM is mis-calibrated (bootstrapped poorly) — wrong placement is worse than no placement.

## My Thoughts

<!-- Add your own notes here -->
