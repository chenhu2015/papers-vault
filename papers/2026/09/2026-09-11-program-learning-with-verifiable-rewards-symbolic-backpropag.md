---
title: "Program Learning with Verifiable Rewards: Symbolic Backpropagation for Post-Training LLMs"
authors: ["Vishvesh Bhat"]
date: 2026-08-28
arxiv_id: "2608.28421v1"
url: "https://arxiv.org/abs/2608.28421"
score: 0.78
topics: [RL training, reward model, agentic RL, RLHF]
status: unread
---

# Program Learning with Verifiable Rewards: Symbolic Backpropagation for Post-Training LLMs

## Summary

PLVR proposes placing reasoning outside model weights as explicit programs of deterministic and neural primitives, trained via symbolic backpropagation: typed ontologies at each program layer, loss at output, and required input ontologies propagated backward by type inference over primitive signatures — credit assignment as a type derivation rather than an estimate. Where RLVR verifies only terminal outcomes, PLVR's reward is a per-step contract verdict dense over program structure. On LiveCodeBench v6 and Tau2Bench, 30B models with PLVR outperform RL by 27.8 points and frontier models 10x larger by 13.6 points.

## Key Contributions

- Programs-as-reasoning: reasoning placed outside model weights as explicit programs composed from deterministic + neural primitives — inspectable, verifiable, transferable across models
- Symbolic backpropagation: typed ontology per layer; credit assigned as type-inference derivation backward through primitive signatures — per-step contract verdict rather than terminal estimate
- Dense per-step reward over program structure: each program layer receives a contract verdict (input/output type match) rather than a single terminal success signal
- Single primitive library transfers across benchmarks (LiveCodeBench v6 + Tau2Bench): marginal cost of a new task is 100 examples of program search with no new fine-tuning

## Relevance

PLVR is the most radical departure from RLVR in the dense-reward-for-RL thread: rather than assigning denser rewards to the same trajectory (T1, TASPO, CRISP), it proposes a different substrate entirely — the reward is dense because the program structure itself is the unit of verification. This connects to the ERPO probe-consensus thread (Sep 09) in that both use execution artifacts as reward, but PLVR's type-contract verdicts are structural (program layer boundaries) whereas ERPO's probe consensus is behavioral (execution agreement). The symbolic backpropagation mechanism is also a deterministic analog of TRIAL's trajectory-relative normalization.

## My Thoughts

<!-- Add your own notes here -->
