---
title: "VERDICT: Training-Free Step-Wise Verification of Multimodal Reasoning via Disagreement-Aware Consensus"
authors: ["Rohit Sinha", "Kunal Tilaganji", "Tanuja Ganu"]
date: 2026-08-11
arxiv_id: "2608.10665v1"
url: "http://arxiv.org/abs/2608.10665v1"
score: 0.72
topics: [multimodal models, vision language models, reward model, VLM]
status: unread
---

# VERDICT: Training-Free Step-Wise Verification of Multimodal Reasoning via Disagreement-Aware Consensus

## Summary

VERDICT provides training-free step-wise verification for multimodal reasoning by formalizing the coupling between disparate frozen verifiers as a disagreement-aware consensus problem — modeled as a coordination game with a unique closed-form equilibrium. The key insight is that disagreement between verifiers on a reasoning step is itself an informative signal: consensus implies validity, while disagreement flags instability, enabling stability-conscious step ranking without labeled supervision. Evaluated across six benchmarks, VERDICT improves over the base model by up to +5.95% and matches domain-specific critics requiring extensive supervision.

## Key Contributions

- **Disagreement-as-signal**: formalizes that cross-verifier disagreement on a reasoning step indicates step unreliability, rather than treating disagreement as noise to be averaged away
- **Coordination game formulation**: models coupled verifier scoring as a coordination game with a unique closed-form equilibrium, enabling efficient consensus computation without iterative optimization
- **Training-free and domain-agnostic**: operates over frozen verifiers with no task-specific fine-tuning; up to +5.95% across 6 benchmarks
- First training-free verifier that makes cross-modal disagreement structure explicit and actionable for step-level filtering and ranking

## Relevance

VERDICT connects to the verifiable process supervision thread from Aug 11 (VPS, VPRM, RLVR-incentivizes-reasoning) and the vault's reward model taxonomy. Where VPS and VPRM focus on defining what counts as a verifiable intermediate step, VERDICT focuses on how to aggregate multiple verification signals when they disagree — a complementary downstream problem. The disagreement-as-signal insight also applies to the SSOPD/BCSD within-group contrast thread: disagreement between rollout branches (correct vs. wrong) is precisely the signal that SSOPD uses to gate the frontier weight, so VERDICT's formalization may provide a theoretical lens for understanding when intra-group contrast is informative.

## My Thoughts

<!-- Add your own notes here -->
