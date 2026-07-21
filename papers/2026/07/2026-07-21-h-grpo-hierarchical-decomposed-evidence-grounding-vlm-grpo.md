---
title: "H-GRPO: Permutation-Invariant Reinforcement Learning for Grounded Visual Reasoning"
authors: ["Eric Peh", "Debaditya Roy", "Basura Fernando"]
date: 2026-07-21
arxiv_id: "2606.29915"
url: "https://arxiv.org/abs/2606.29915"
score: 0.76
topics: [multimodal models, vision language models, GRPO, VLM, vision-language]
status: unread
---

# H-GRPO: Permutation-Invariant Reinforcement Learning for Grounded Visual Reasoning

## Summary

H-GRPO addresses hallucination in VLM reasoning by decomposing global queries into atomic sub-questions each requiring an explicit sub-answer and a localized bounding-box evidence region, constructing a structured reasoning path where the final answer emerges as a logical consequence of verified visual facts. A permutation-invariant GRPO training formulation prevents option-ordering artifacts from contaminating the visual grounding reward signal (analogous to ACRE's option-shuffling consistency reward). A 4B model trained with H-GRPO outperforms 7B grounding LLMs and SAM3 across PascalPart, PartImageNet, and InstructPart benchmarks and transfers to reasoning segmentation.

## Key Contributions

- De-compositional Evidence Grounding (DEG): forces decomposition of global queries into atomic sub-questions each with an explicit sub-answer and a localized bounding-box evidence region
- Structured reasoning path: final answer is a logical consequence of verified visual facts, not a direct pattern match — mimics human-like deduction via verified sub-steps
- Permutation-invariant GRPO: training formulation that prevents option-ordering bias from corrupting the grounding reward signal
- Parameter efficiency: 4B model outperforming 7B alternatives, suggesting explicit structural decomposition is a stronger inductive bias than scale for grounding tasks

## Relevance

H-GRPO connects the VLM RL faithfulness thread (CORA, SIVA-RL, DyCo-RL, FWS) with the structured reasoning / credit assignment thread. The bounding-box evidence requirement for each sub-question is a spatial analogue to the step-level process supervision in FaithRL and BetaPRM — in all three cases, the key insight is that outcome-level rewards alone cannot enforce intermediate reasoning quality. The permutation-invariant GRPO formulation also closes an option-ordering gap in grounding tasks that ACRE identified for VQA, confirming that this artifact generalizes across VLM RL task types.

## My Thoughts

<!-- Add your own notes here -->
