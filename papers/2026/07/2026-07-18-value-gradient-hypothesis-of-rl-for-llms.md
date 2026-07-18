---
title: "Value-Gradient Hypothesis of RL for LLMs"
authors: ["Arip Asadulaev", "Daniil Ognev", "Karim Salta", "Martin Takac"]
date: 2026-05-20
arxiv_id: "2605.21654"
url: "https://arxiv.org/abs/2605.21654"
score: 0.87
topics: [GRPO, PPO, RL training, reinforcement learning, agentic RL]
status: unread
---

# Value-Gradient Hypothesis of RL for LLMs

## Summary

Develops a theoretical value-gradient perspective explaining why critic-free RL methods (PPO, GRPO) work for LLM post-training without explicit value estimates. Shows that actor updates are value-gradient-like in expectation — the backward pass propagates costates whose conditional expectation equals the value gradient — and for discrete transformers, attention autodifferentiation produces empirical costates approximating this value signal with error controlled by sampling gap and policy entropy. Provides a decomposition of RL impact into value gradient signal strength and reachable reward headroom, yielding a principled criterion for predicting when RL post-training will be most effective along a pretraining trajectory.

## Key Contributions

- Under differentiable rollout and additive-noise parameterization, proves actor update is value-gradient-like in expectation: backward pass costates equal value gradient in conditional expectation
- For discrete transformer policies, shows attention autodifferentiation produces empirical costates approximating value signal; error controlled by sampling gap and policy entropy
- Decomposes RL impact into two orthogonal factors: value gradient signal strength (how informative gradients are) and reachable reward headroom (how much improvement remains)
- Criterion for predicting when RL post-training is most effective: requires both strong gradient signal and non-trivial headroom

## Relevance

Directly addresses the open theoretical question behind the vault's GRPO optimization internals thread (RIPO, EGRSD, Prune-OPD, TurnOPD): RIPO fixed the geometry, but *why* does the gradient signal in critic-free methods carry useful value information at all? This paper provides the answer. The headroom criterion is also the most principled account to date of why SFT→RL staging works (SFT saturates headroom; RL exploits remaining headroom that SFT can't reach).

## My Thoughts

<!-- Add your own notes here -->
