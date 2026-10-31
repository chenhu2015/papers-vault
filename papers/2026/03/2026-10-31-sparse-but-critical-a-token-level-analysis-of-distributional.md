---
title: "Sparse but Critical: A Token-Level Analysis of Distributional Shifts in RLVR Fine-Tuning of LLMs"
authors: ["Haoming Meng", "Kexin Huang", "Shaohang Wei", "Chiyu Ma", "Shuo Yang", "Xue Wang", "Guorui Wang", "Bolin Ding", "Jingren Zhou"]
date: 2026-10-31
arxiv_id: "2603.22446v1"
url: "http://arxiv.org/abs/2603.22446v1"
score: 0.84
topics: [reinforcement learning, RLHF, RLAIF, GRPO, RL training]
status: unread
---

# Sparse but Critical: A Token-Level Analysis of Distributional Shifts in RLVR Fine-Tuning of LLMs

## Summary

Systematic empirical study showing RLVR fine-tuning induces highly sparse, targeted token-level distributional shifts — only a small fraction of token distributions meaningfully diverge between base and RL policies. Cross-sampling interventions reveal that inserting a small number of RL-sampled tokens into base generations progressively recovers RL performance, while injecting similarly few base tokens into RL generations collapses performance to base levels, isolating the critical token set. Divergence-weighted advantage variants that focus credit assignment on these sparse critical tokens yield further improvements over standard RLVR.

## Key Contributions

- Shows RLVR shifts are sparse: only a small fraction of token distributions exhibit meaningful divergence between base and RL model
- Cross-sampling experiment: swap RL/base token choices at specific positions to isolate causal contribution of sparse shifts to performance gains
- Characterises shift structure: token entropy, positional concentration, probability mass reallocation
- Divergence-weighted advantage variants improve over standard RLVR baselines

## Relevance

Provides the empirical token-level foundation for the GRPO training dynamics thread. The "There Is No Free Lunch in RLVR" theorem (today) proves the pass@1/pass@k tradeoff algebraically; this paper shows *where in the sequence* that tradeoff is executed — a small number of critical token decisions. The two papers together explain both the macro statistics (pass@1 up, pass@k down) and the micro mechanism (sparse critical positions). Published March 2026, newly surfaced today.

## My Thoughts

<!-- Add your own notes here -->
