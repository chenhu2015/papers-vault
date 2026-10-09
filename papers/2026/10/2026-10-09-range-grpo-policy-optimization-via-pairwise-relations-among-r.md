---
title: "Range-GRPO: Policy Optimization via Pairwise Relations among Reward Intervals"
authors: ["Ryunyi Lee", "Kangjun Noh", "Somin Kim", "Heedong Kim", "Kyungwoo Song"]
date: 2026-10-01
arxiv_id: "2610.01548"
url: "https://arxiv.org/abs/2610.01548"
score: 0.78
topics: [GRPO, RL training, reward model, RLHF]
status: unread
---

# Range-GRPO: Policy Optimization via Pairwise Relations among Reward Intervals

## Summary

Range-GRPO replaces point reward comparisons in GRPO with pairwise comparisons of conformally calibrated reward intervals, so that reward uncertainty from LLM-as-Judge pseudo-rewards influences both the magnitude and direction of policy gradient signals. It operates semi-supervised over labeled and unlabeled prompts, and theoretical analysis shows it recovers the Dr.GRPO advantage when all intervals collapse to points. Empirical results show the best in-distribution and out-of-distribution average performance among evaluated semi-supervised methods at lower training cost.

## Key Contributions

- Conformally calibrated reward ranges: represent pseudo-rewards as uncertainty-aware intervals rather than point scores from LLM judges
- Pairwise interval comparison in GRPO: when intervals overlap, the comparison direction becomes probabilistic — uncertainty affects gradient signal magnitude and direction simultaneously
- Theoretical connection: recovers Dr.GRPO advantage as a degenerate case (zero-width intervals)
- Semi-supervised GRPO: trains on both reference-answer-labeled and unlabeled prompts without requiring full verifier coverage

## Relevance

Addresses a practical limitation of the GRPO-based training thread: in domains without reference answers or executable verifiers, LLM-as-Judge produces uncertain scores. Range-GRPO provides a principled way to incorporate that uncertainty directly into the GRPO update, connecting to the reward hacking / reward design cluster (BoT-GRPO, EnGRICH, LatentGRM from Oct 8) and to the BoT-GRPO open question about mis-calibrated token-level RMs — interval calibration could bound the uncertainty introduced by a bootstrapped PRM.

## My Thoughts

<!-- Add your own notes here -->
