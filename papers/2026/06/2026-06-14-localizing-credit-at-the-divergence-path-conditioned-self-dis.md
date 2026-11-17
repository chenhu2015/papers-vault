---
title: "Localizing Credit at the Divergence: Path-Conditioned Self-Distillation for LLM Reasoning"
authors: ["(see arxiv 2606.15576)"]
date: 2026-06-14
arxiv_id: "2606.15576"
url: "https://arxiv.org/abs/2606.15576"
score: 0.85
topics: [RL training, RLHF, RLAIF, OPSD, reward model]
status: unread
---

# Localizing Credit at the Divergence: Path-Conditioned Self-Distillation for LLM Reasoning

## Summary

Proposes HSD (Hindsight Self-Distillation), which conditions the teacher on a successful peer rollout drawn from the current training group rather than on the ground-truth answer. Since a peer rollout is an exact sample from the success-conditioned policy, no additional sampling is needed; the resulting credit signal concentrates at the divergence position between a failed rollout and its successful peer, providing precise path-level guidance at the token positions where it matters most. Outperforms GRPO variants and standard OPSD on math and code benchmarks, with the largest gains on terse-answer tasks like AIME where endpoint-only teacher context is weakest.

## Key Contributions

- Peer-rollout teacher: conditions on a successful group member rather than ground-truth answer, requiring zero additional rollouts
- Credit concentrates at the divergence position between failed and successful paths — the exact token position where path-level guidance is most needed
- Largest gains on terse-answer tasks (AIME) where endpoint-only PI is least informative
- Demonstrates that the teacher's PI source matters as much as the distillation objective

## Relevance

Directly complements ROSD (Beyond Imitation, 2605.28014) which also avoids full-trajectory imitation — ROSD uses reflective contrast between failed+correct rollouts; HSD uses peer-conditioned teacher with divergence-localized credit. Both share the insight that endpoint-answer PI is insufficient. HSD is a more elegant zero-cost solution: the peer rollout is already sampled by the training group. This adds a third distinct teacher-conditioning mechanism to the OPSD cluster.

## My Thoughts

<!-- Add your own notes here -->
