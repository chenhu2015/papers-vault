---
title: "There Is No Free Lunch in RLVR: Every pass@1 Gain Has a pass@k Price"
authors: ["Yinuo Liu"]
date: 2026-10-31
arxiv_id: "2610.39295v1"
url: "http://arxiv.org/abs/2610.39295v1"
score: 0.88
topics: [reinforcement learning, agentic RL, GRPO, RLHF, RLAIF]
status: unread
---

# There Is No Free Lunch in RLVR: Every pass@1 Gain Has a pass@k Price

## Summary

RLVR provably raises pass@1 while strictly lowering pass@k at large sampling budgets, proven via an exponential tilt model of policy updates over strategies shared across prompts. The pass@1 vs. pass@k reversal is an exact, computable price via Stiemke duality — not a training artifact — and a constrained update traces the precise frontier; removing the crossover entirely costs the entire pass@1 gain. The same tilt identity unifies entropy collapse and the entropy-performance law under one mechanism, with a diagnostic that reads the price from any evaluation log.

## Key Contributions

- Proves via exponential tilt model that every RLVR pass@1 gain strictly lowers pass@k success on some prompts (Stiemke duality condition)
- Computes the exact price: number of crossovers is bounded by sign variation in the per-prompt success shift, a totally positive bound that is tight
- Shows the reversal is not a bug: a constrained update traces the exact pass@1 vs. pass@k Pareto frontier
- Unifies entropy collapse and the entropy-performance law under the same tilt identity, identifying an exponent

## Relevance

Directly targets the GRPO/RLVR training dynamics thread — the theorem makes the pass@1 / pass@k tradeoff measurable and exact, explaining phenomena that had been empirically observed but not formally characterized. Connects to Beacon's advantage collapse finding and the entropy analysis in PAEC/UCAS: all are manifestations of the same underlying tilt mechanism.

## My Thoughts

<!-- Add your own notes here -->
