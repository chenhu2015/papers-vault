---
title: "Entropy-Gated Selective Policy Optimization: Token-Level Gradient Allocation for Hybrid Training of Large Language Models"
authors: ["Anonymous"]
date: 2026-07-08
arxiv_id: "2602.03309v1"
url: "https://arxiv.org/abs/2602.03309"
score: 0.78
topics: [RL training, RLHF, PPO, reward model, agentic RL]
status: unread
---

# Entropy-Gated Selective Policy Optimization: Token-Level Gradient Allocation for Hybrid Training of Large Language Models

## Summary

Proposes EGSPO, a three-stage hybrid SFT+RL framework that extends sample-level mixing with token-level gradient modulation via predictive entropy gating: high-entropy tokens receive full PPO updates (encouraging exploration at uncertain positions) while low-entropy tokens receive attenuated updates (reducing variance and preserving established knowledge). Both branches incorporate the advantage function to ensure incorrect trajectories receive consistent negative learning signals, preventing reinforcement of confident errors. Achieves +3.8% on AIME and +2.9% on MATH over CHORD baseline with only 3.4% additional computational overhead.

## Key Contributions

- Token-level entropy gate: routes per-token gradient contributions based on predictive entropy, replacing the binary sample-level SFT/RL split with a continuous per-token allocation
- Advantage-conditioned gating in both branches: unlike hard masking that ignores advantage for low-entropy tokens, EGSPO attenuates but preserves the advantage signal, preventing reinforcement of confident wrong predictions
- Three-stage pipeline: SFT warm-up → rollout generation with entropy computation → entropy-gated PPO update; adds minimal overhead at 3.4% extra compute
- Validates on AIME (+3.8%) and MATH (+2.9%) benchmarks over CHORD baseline

## Relevance

EGSPO is the token-level entropy analog of GRPO-λ's (today) eligibility-trace credit weighting: both papers use the model's own distributional signal to differentiate gradient contributions at the token level, but where GRPO-λ uses discounted future rewards (TD credit), EGSPO uses current predictive entropy (exploration uncertainty). The entropy-gate is also structurally related to ConsistRoll's (Jul 7) cross-view reward — both papers identify that uniform gradient treatment across all tokens/views is wasteful, and both introduce a signal-dependent weighting that preserves diversity. The specific treatment of low-entropy tokens (attenuated but not zero advantage) addresses the same problem as SeL (information self-locking): high-confidence wrong predictions would otherwise dominate the learning signal if entropy gating used hard masking.

## My Thoughts

<!-- Add your own notes here -->
