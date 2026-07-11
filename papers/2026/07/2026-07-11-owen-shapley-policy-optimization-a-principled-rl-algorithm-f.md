---
title: "Owen-Shapley Policy Optimization: A Principled RL Algorithm for Generative Search LLMs"
authors: ["Abhijnan Nath", "Alireza Bagheri Garakani", "Tianchen Zhou", "Fan Yang", "Yan Gao", "Nikhil Krishnaswamy"]
date: 2026-07-11
arxiv_id: "2601.08403"
url: "https://arxiv.org/abs/2601.08403"
score: 0.78
topics: [reward model, RL training, GRPO, agentic RL]
status: unread
---

# Owen-Shapley Policy Optimization: A Principled RL Algorithm for Generative Search LLMs

## Summary

OSPO redistributes sequence-level GRPO advantages based on each token segment's marginal contribution to the outcome via Shapley-Owen attributions, forming coalitions over semantically coherent units (phrases, sentences) and applying potential-based reward shaping without a parametric value model. This addresses the credit assignment gap in standard GRPO where sparse sequence-level rewards obscure which response parts drive performance, particularly for tasks requiring inference of latent user intent from under-specified language. Consistent gains over baselines with notable OOD robustness to unseen retrievers at test time.

## Key Contributions

- Shapley-Owen attribution over semantically coherent segments: forms coalitions of phrases/sentences to compute each segment's marginal contribution to the outcome reward
- Potential-based reward shaping: transforms Shapley-Owen attributions into sub-sequence reward shaping that preserves the optimal policy (no policy-optimal distortion)
- Value-model-free: achieves segment-level credit without adding a learned critic, making it directly integrable into GRPO pipelines at MRPO-comparable overhead
- OOD robustness: trained on fixed retrievers but generalizes to unseen retrievers, suggesting credit attribution reduces over-reliance on retriever-specific patterns

## Relevance

OSPO is the fifth approach to sub-sequence credit assignment in the vault after MRPO (manual temporal position schedule), GRPO-λ (TD eligibility traces), EGSPO (entropy-gated token routing), and ROSE's length-aware segment advantage. OSPO's game-theoretic Shapley attribution is the most formally principled: it uniquely satisfies efficiency, symmetry, dummy, and additivity axioms simultaneously. The game-theoretic framing also connects to UnityMAS-O's role-level credit (Jul 10) — both decompose global rewards into agent/segment contributions using cooperative game theory, but at different granularities (sequence segments vs. multi-agent roles).

## My Thoughts

<!-- Add your own notes here -->
