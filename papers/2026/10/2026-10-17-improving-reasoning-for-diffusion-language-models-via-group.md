---
title: "Improving Reasoning for Diffusion Language Models via Group Diffusion Policy Optimization"
authors: ["Kevin Rojas", "Jiahe Lin", "Kashif Rasul", "Anderson Schneider", "Yuriy Nevmyvaka", "Molei Tao", "Wei Deng"]
date: 2025-10-09
arxiv_id: "2510.08554v3"
url: "http://arxiv.org/abs/2510.08554v3"
score: 0.82
topics: [reinforcement learning, RL training, GRPO, agentic RL]
status: unread
---

# Improving Reasoning for Diffusion Language Models via Group Diffusion Policy Optimization

## Summary

GDPO addresses RL fine-tuning for diffusion language models (DLMs) where token-level likelihoods are intractable: prior diffu-GRPO used severely biased one-step unmasking estimates. GDPO replaces these with an ELBO-based sequence-level surrogate and applies Semi-deterministic Monte Carlo integration to reduce variance at tight evaluation budgets, yielding provably lower variance than vanilla double-MC ELBO sampling. Outperforms diffu-GRPO on math, reasoning, and coding benchmarks.

## Key Contributions

- Decomposes the ELBO estimator's variance sources and identifies which dimensions can be evaluated deterministically without extra cost
- Semi-deterministic Monte Carlo: integrates analytically over fast-converging dimensions, retaining stochasticity only where the ELBO is most sensitive
- Provably lower-variance bound vs. vanilla double Monte Carlo sampling under tight evaluation budgets
- SOTA on math, reasoning, and coding vs. diffu-GRPO; consistent gains across pretrained checkpoints

## Relevance

GDPO completes a two-paper picture of principled RL for diffusion LMs started by PACT (Oct 16): PACT provides potential-anchored step-level credit assignment for denoising trajectories, while GDPO provides a lower-variance policy optimisation objective for the same model class. Both papers together now motivate tracking the diffusion LM RL space as a separate thread.

## My Thoughts

<!-- Add your own notes here -->
