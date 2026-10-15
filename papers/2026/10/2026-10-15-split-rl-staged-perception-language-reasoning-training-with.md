---
title: "SPLIT-RL: Staged Perception-Language Reasoning Training with Claim-Level Advantages"
authors: ["Raja Kumar", "Rajat Koner", "Ritwick Chaudhry", "Zhuowei Li", "Nishant Sankaran", "Yifan Xing"]
date: 2026-10-15
arxiv_id: "2610.10889v1"
url: "https://arxiv.org/abs/2610.10889"
score: 0.90
topics: [agentic RL, VLM, vision-language, GRPO, reward model, multimodal]
status: unread
---

# SPLIT-RL: Staged Perception-Language Reasoning Training with Claim-Level Advantages

## Summary

SPLIT-RL separates VL reasoning post-training into disjoint visual reasoning (VR) and language reasoning (LR) phases so group-relative advantages isolate one capability at a time. Its CLA-GRPO variant decomposes VR-phase rollouts into atomic visual claims and assigns fine-grained claim-level advantages via visual-type group formation. Oracle diagnostics confirm that standard answer-only GRPO leaves visual perception unchanged, while SPLIT-RL improves both VR and LR capabilities.

## Key Contributions

- Phase disjointness: VR and LR trained in separate phases so group-relative advantages are capability-specific, not entangled
- CLA-GRPO: decompose VR rollouts into atomic visual claims; form groups by visual-type; assign claim-level advantages
- Phase-specific reward design: distinct reward signals for each phase, not a single final-answer reward
- Oracle diagnostic showing GRPO improves LR only; SPLIT-RL improves both VR and LR (+1.4–6.1 points on Qwen3-VL 2B–30B)
- Single CoT inference pass: no overhead at test time despite two-phase training

## Relevance

Provides the strongest empirical evidence yet that standard GRPO's flat trajectory-level advantage is causally responsible for perception stagnation — not just correlated with it. The claim-level advantage in CLA-GRPO is structurally similar to OWLET's token-level evidence weighting but works at the semantic claim level rather than the likelihood-differential level, suggesting complementary granularities within the same VLM RL credit thread.

## My Thoughts

<!-- Add your own notes here -->
