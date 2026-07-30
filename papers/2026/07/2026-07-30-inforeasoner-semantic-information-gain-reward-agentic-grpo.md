---
title: "Optimizing Agentic Reasoning with Retrieval via Synthetic Semantic Information Gain Reward"
authors: ["Senkang Hu", "Yong Dai", "Yuzhi Zhao", "Yihang Tao", "Yu Guo", "Zhengru Fang", "Sam Tak Wu Kwong", "Yuguang Fang"]
date: 2026-07-30
arxiv_id: "2602.00845v3"
url: "http://arxiv.org/abs/2602.00845v3"
score: 0.82
topics: [agentic RL, RL training, GRPO, LLM agent, reward model]
status: unread
---

# Optimizing Agentic Reasoning with Retrieval via Synthetic Semantic Information Gain Reward

## Summary

InfoReasoner redefines information gain for agentic retrieval as uncertainty reduction over the model's belief states, with theoretical proofs of non-negativity, telescoping additivity, and channel monotonicity — properties that make the reward composable across turns in the same way CIGPO's per-turn IG decomposes Progress Advantage. Unlike CIGPO and IGPO which estimate IG from log-likelihood changes in the reference model, InfoReasoner uses an output-aware intrinsic estimator via semantic clustering over bidirectional textual entailment, enabling IG estimation without a reference model. Trained with GRPO, achieves up to 5.4% average accuracy improvement across 7 QA benchmarks over strong retrieval-augmented baselines.

## Key Contributions

- Theoretically grounded IG definition: uncertainty reduction over belief states, with proofs of non-negativity, telescoping additivity, and channel monotonicity
- Output-aware intrinsic estimator using semantic clustering via bidirectional textual entailment — no reference model required
- Unified framework (InfoReasoner) combining IG intrinsic reward with GRPO for multi-turn agentic retrieval
- Validated on 7 QA benchmarks; 5.4% average accuracy improvement over retrieval-augmented baselines

## Relevance

InfoReasoner is the reference-model-free member of the IG-based credit assignment family (IGPO Oct 2025 → InfoReasoner Jan 2026 → InfoPO Feb 2026 → CIGPO Jul 2026). Its telescoping additivity proof is structurally important: it formally establishes that per-turn IG rewards can be summed across turns to yield the total IG over a trajectory, which is the mathematical guarantee that CIGPO's decomposition of Progress Advantage is well-defined. This property was implicit in CIGPO's empirical success but had not been proved; InfoReasoner's theoretical contribution retroactively provides the foundation.

## My Thoughts

<!-- Add your own notes here -->
