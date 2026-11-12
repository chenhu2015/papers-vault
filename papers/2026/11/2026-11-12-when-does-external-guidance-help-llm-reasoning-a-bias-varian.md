---
title: "When Does External Guidance Help LLM Reasoning? A Bias-Variance Theory of Guidance-Augmented GRPO"
authors: ["Sofia Torres", "Gabriel Almeida", "Carter Adams", "Camila Rocha"]
date: 2026-11-12
arxiv_id: "2610.06861v1"
url: "https://arxiv.org/abs/2610.06861"
score: 0.84
topics: [agentic RL, RL training, GRPO, reward model]
status: unread
---

# When Does External Guidance Help LLM Reasoning? A Bias-Variance Theory of Guidance-Augmented GRPO

## Summary

GA-GRPO formalises external guidance (expert traces, self-explanations, retrieved thought patterns) as a stochastic guidance operator G that re-weights the question distribution, casting the resulting policy-gradient estimator as biased on-policy with bias bounded by total-variation guidance divergence δ_G. The framework subsumes LUFFY, ExPO, PAPO, and TAPO as special cases and proves O(1/√T) convergence to an O(δ√T)-neighbourhood, together with a closed-form MSE-optimal guidance weight λ*(T,δ,σ²). Experiments on Qwen2.5-Math-7B-Base confirm optimal-weight GA-GRPO matches or surpasses all baselines while using 31% fewer GPU-hours.

## Key Contributions

- Unified theoretical framework (GA-GRPO) that subsumes LUFFY, ExPO, PAPO, and TAPO as special cases via different choices of guidance operator G
- Formal proof: O(1/√T) convergence to O(δ√T)-neighbourhood of GRPO stationary point, with matching minimax lower bound showing Ω(δ²T) bias is unavoidable
- Closed-form MSE-optimal guidance weight λ*(T,δ,σ²) = σ²/(σ² + R²_max δ²T) derived analytically
- 31% GPU-hour reduction at matched or superior accuracy versus all comparison methods on nine benchmarks

## Relevance

Directly advances the GRPO training dynamics thread (now 16+ entries): this is the first paper to give a principled convergence theory for guidance-augmented GRPO, explaining why empirical gains from LUFFY/ExPO are possible and when they are bounded. The optimal λ* formula is immediately actionable and the bias-variance framing connects to the exploration/diversity thread (δ_G measures how far guidance pushes the sampling distribution from the policy's own distribution).

## My Thoughts

<!-- Add your own notes here -->
