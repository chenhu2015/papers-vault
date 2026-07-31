---
title: "Beyond Entropy: Learning from Token-Level Distributional Deviations for LLM Reasoning"
authors: ["Xuanzhi Feng", "Zhengyang Li", "Zeyu Liu", "Haoxi Li", "Yuming Jiang", "Bing Guo", "Jingcai Guo", "Jie Zhang", "Song Guo"]
date: 2026-07-31
arxiv_id: "2606.19771"
url: "https://arxiv.org/abs/2606.19771"
score: 0.78
topics: [RL training, GRPO, reward model, multimodal models]
status: unread
---

# Beyond Entropy: Learning from Token-Level Distributional Deviations for LLM Reasoning

## Summary

ICT (Independent Combinatorial Tokens) uses Jensen-Shannon divergence between token logit distributions to identify tokens with distinctive distributional patterns as critical branching points for guiding exploration in LLM RL, specifically addressing the dual pathology of entropy collapse (from uniform token updates) and entropy explosion (from naive entropy maximization). Theoretical analysis using both Shannon and second-order Rényi entropy proves that selectively updating divergence-identified tokens simultaneously reduces overall distribution uncertainty while controlling probability concentration. Updating only the top-10% unique tokens on Qwen2.5 achieves 4.58% average pass@4 improvement and up to 14.9% maximum gain over GRPO, STAPO, and 20-Entropy baselines across seven benchmarks.

## Key Contributions

- JS divergence between token logit distributions as a measure of "distributional distinctiveness" for identifying critical branching points
- Dual theoretical guarantee: selective updates simultaneously reduce Shannon entropy (randomness control) and Rényi entropy (concentration control), preventing both collapse and explosion
- Unified framework for the entropy-collapse vs. entropy-explosion tradeoff without hyperparameter tuning between them
- Validated on 0.5B/1.5B/7B Qwen2.5 models across math, commonsense, and Olympiad-level benchmarks

## Relevance

ICT adds a fifth distinct signal to the entropy-as-structural-signal family (Gap #12): Shannon entropy (STAPO), multi-rollout frequency (O²-CritiCuRL), post-tool-call entropy bonus (TAO-RL), surprisal quantiles (STARE), and now JS divergence over logit distributions (ICT). The JS divergence angle is the most information-theoretically principled of the five: rather than measuring the model's own uncertainty, it measures how much a token's distribution *deviates from the reference distribution* — connecting directly to the IG-based credit family (IGPO/CIGPO). The dual Rényi guarantee is the strongest theoretical result in the family, providing formal control over both tails of the entropy distribution simultaneously.

## My Thoughts

<!-- Add your own notes here -->
