---
title: "ANCORA: Learning to Question via Manifold-Anchored Self-Play for Verifiable Reasoning"
authors: ["Chengcao Yang"]
date: 2026-04-30
arxiv_id: "2604.27644v2"
url: "https://arxiv.org/abs/2604.27644"
score: 0.80
topics: [agentic RL, GRPO, RL training, reinforcement learning]
status: unread
---

# ANCORA: Learning to Question via Manifold-Anchored Self-Play for Verifiable Reasoning

## Summary

ANCORA introduces open-ended curriculum self-play where a unified policy alternates between Proposer (generating novel verifiable problems) and Solver (producing verified solutions), using a two-level GRPO update that couples advantages across problem specifications and solution attempts simultaneously. A UCB-guided Curriculum DAG ensures the training problem set provably expands under self-composition, and iterative self-distilled SFT anchors the base model before RL to prevent Proposer collapse under sparse verifier feedback. Applied to formal verification in Verus, ANCORA raises pass@1 from 26.6% to 81.5% without any human-annotated solutions.

## Key Contributions

- Unified Proposer/Solver self-play: same model generates problems AND solves them, bootstrapping from zero human solutions
- Two-level GRPO update coupling Proposer advantages (across specifications) with Solver advantages (across solution attempts)
- UCB-guided Curriculum DAG that provably expands the training problem set under self-composition
- Iterative self-distilled SFT as stabilizer: projects base model onto valid-output manifold before RL to prevent Proposer collapse

## Relevance

Directly addresses the self-play / synthetic problem generation thread that had failed at arxiv title level (Jun 11 attempt returned off-target results). ANCORA is precisely this paradigm — the agent generates its own training tasks via the Proposer role, eliminating dependence on human-curated problem sets. The two-level GRPO extends the interest profile's GRPO keyword to a novel dual-role setting, and the UCB curriculum DAG connects to the FORT-Searcher (Jun 11) finding that data quality is the key bottleneck for agentic RL.

## My Thoughts

<!-- Add your own notes here -->
