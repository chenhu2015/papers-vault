---
title: "Same Luck, Different Choice: Twin-World Credit Assignment for Agentic Reinforcement Learning"
authors: ["Zeropy Surio", "Tobias Engel", "Mei-Lin Chou", "Anika Raman", "Samuel Okafor"]
date: 2026-10-22
arxiv_id: "2610.31544v2"
url: "https://arxiv.org/abs/2610.31544"
score: 0.85
topics: [agentic RL, GRPO, RL training]
status: unread
---

# Same Luck, Different Choice: Twin-World Credit Assignment for Agentic Reinforcement Learning

## Summary

TWICE eliminates outcome-noise conflation in counterfactual credit estimation by constructing twin rollouts that share the identical Gumbel token-sampling noise as the factual episode but diverge at the target decision point, so outcome differences reflect the decision alone. This reduces sample complexity from Θ(Δ⁻²) to Θ(Δ⁻¹) for resolving advantages of size Δ, with a square-root budget rule concentrating twins where outcomes are predicted to disagree. Improves GRPO exact match by 5.3/4.5 points on Qwen2.5-3B/7B across 7 QA benchmarks, outperforming tree-search and counterfactual-branching baselines while using 68% fewer auxiliary tokens than VinePPO.

## Key Contributions

- Gumbel noise keying by turn+line enables exact twin worlds in deterministic agentic environments (retriever, corpus, grader are deterministic)
- Formal proof that twin credit is unbiased and reduces variance by factor (1−ρ) where ρ is twin outcome correlation
- Square-root budget rule allocates twins to maximize expected variance reduction per token
- 68% token reduction vs VinePPO at comparable or better accuracy on 7 QA benchmarks

## Relevance

Directly in the agentic credit assignment thread, with an orthogonal angle to MSPO/ViCARD (which fix *how* credit is assigned) — TWICE fixes the *measurement* problem: existing counterfactual estimates conflate decision effects with downstream sampling luck. The key insight that agentic environments are often deterministic given the sampling noise enables the coupling trick.

## My Thoughts

<!-- Add your own notes here -->
