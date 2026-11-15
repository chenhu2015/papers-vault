---
title: "A Stronger Teacher Within: Strengthening MoE Models via On-Policy Bidirectional Distillation"
authors: ["Haoyu Chen", "Jun Bai", "Yang Liu"]
date: 2026-10-16
arxiv_id: "2610.23185"
url: "https://arxiv.org/abs/2610.23185"
score: 0.76
topics: [RLVR, RL training, reward model, agentic RL, RLAIF]
status: unread
---

# A Stronger Teacher Within: Strengthening MoE Models via On-Policy Bidirectional Distillation

## Summary

MoEvolve solves the teacher-availability problem in RLVR by exploiting the MoE architecture itself: activating more experts per token (high-k) exposes latent capacity that acts as a stronger self-teacher, but naive expansion degrades performance since co-activated experts weren't jointly optimized. Following a recovery-then-improvement strategy, MoEvolve first restores and strengthens the high-k model via RLVR, then reverses direction to distill enhanced capabilities back into the original low-k configuration. Final low-k models improve over initial models by up to 22.2 domain-average points and outperform same-budget RLVR baselines by up to 6.5 points, with the low-k often exceeding its expanded teacher.

## Key Contributions

- Insight: MoE activation-budget expansion creates an architecturally-grounded stronger self-teacher without hand-designed privileged information
- Recovery-then-improvement: restore high-k model quality, then strengthen via RLVR with expanded capacity
- Bidirectional distillation: teacher→student then student←teacher direction reversal
- Low-k models outperform RLVR baselines by up to 6.5 pts, often surpassing their high-k teachers
- Up to 22.2 domain-average point improvement over initial models across diverse MoE architectures/benchmarks

## Relevance

Extends the parameter-efficient RL cluster (T-Router, GrowRL, Deletion Tuning) with a new mechanism: architectural self-expansion as self-teacher. Also connects to the GIFT/EPIC/LGPO thread on making distillation compatible with RL — MoEvolve provides an architecture-native route that avoids the gradient-conflict problem by sequencing the two objectives rather than mixing them.

## My Thoughts

<!-- Add your own notes here -->
