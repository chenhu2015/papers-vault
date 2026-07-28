---
title: "Hybrid Advantage Estimation with Unified Critic for VLM Agentic Reinforcement Learning"
authors: ["Wenxuan Zhang", "Yuhui Wang", "Donggang Jia", "Xiaoqian Shen", "Jian Ding", "Ivan Viola", "Jürgen Schmidhuber", "Mohamed Elhoseiny"]
date: 2026-07-28
arxiv_id: "2607.23605"
url: "https://arxiv.org/abs/2607.23605"
score: 0.91
topics: [agentic RL, vision language models, VLM, multimodal models, RL training, GRPO, LLM agent]
status: unread
---

# Hybrid Advantage Estimation with Unified Critic for VLM Agentic Reinforcement Learning

## Summary

Establishes theoretical formulations for both token-level and turn-level RL objectives in VLM agentic settings and derives a hybrid advantage that jointly serves both, then proves that a single unified critic with an appropriate discount factor and learning target can estimate values for both granularities simultaneously. HyGAE (Hybrid Generalized Advantage Estimation), the resulting actor-critic framework, achieves 91% average success rate across five multi-turn decision-making environments — a +10% improvement over competing methods — and ablations confirm the exact analytic form of the hybrid advantage is critical for stable optimization.

## Key Contributions

- Theoretical formulations of token-level and turn-level RL objectives as distinct but complementary optimization targets in VLM multi-turn settings
- Derivation of the hybrid advantage: a single signal that simultaneously satisfies both token-wise and turn-wise gradient objectives
- Proof that with appropriate discount factor and learning target, a single unified critic can estimate values for both granularities without separate networks
- HyGAE actor-critic framework achieving 91% avg success on 5 multi-turn environments, +10% over prior SOTA

## Relevance

Progress Advantage (Jul 26) proved log π_RL/π_ref is the optimal advantage for general stochastic MDPs; HyGAE specializes this to VLM multi-turn agentic settings, providing a unified critic formulation that bridges the token-level credit (PRPO, Jul 26) and turn-level credit (TRACE, Jul 25) strands of the credit assignment thread — the first paper to prove these objectives can be served by a single critic with theoretical guarantees.

## My Thoughts

<!-- Add your own notes here -->
