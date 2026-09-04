---
title: "LLMs as a Jury: Cross-Model Consensus Can Outperform Process Reward Models for LLM Reasoning"
authors: ["Ning Liu"]
date: 2026-09-04
arxiv_id: "2607.10139v3"
url: "http://arxiv.org/abs/2607.10139v3"
score: 0.73
topics: [reward model, reinforcement learning, RLHF, RLAIF, LLM agent]
status: unread
---

# LLMs as a Jury: Cross-Model Consensus Can Outperform Process Reward Models for LLM Reasoning

## Summary

LLM-jury proposes cross-model consensus — the degree to which independently trained models agree on a final answer — as a test-time verifier that requires no reward model training or inter-model scoring. A closed-form parameter-free law predicts jury accuracy from three panel statistics (MAE 0.03), characterizing when to trust the jury and where it fails (shared-error floor near zero on math, non-trivial on science). Across seven benchmarks, the free jury matches the strongest trained verifier within its training domain and is top selector outside it — directly relevant to the reward model thread: Demystifying RL Post-Training showed RL success depends on reward signal quality; LLM-jury shows a free alternative to trained PRMs/ORMs for that signal.

## Key Contributions

- Cross-model consensus as a parameter-free verifier: error decorrelation means independently trained models err differently, so correct answers accumulate agreement while wrong answers scatter
- Closed-form prediction law: jury accuracy predicted from three panel statistics to MAE 0.03, exposing ceiling (shared-error floor) and applicability conditions in advance
- Outperforms self-consistency and self-scoring; matches strongest trained verifier in-domain, best selector out-of-domain across seven benchmarks
- Complementary to Agon (Sep 04): LLM-jury uses multi-model consensus at test time; Agon bakes rival grading into training — both replace static reward models, from different directions

## Relevance

LLM-jury connects to the reward model thread (Q-RM Sep 03, Demystifying RL Post-Training Sep 03) from the verification side. Q-RM showed that generative token probabilities create a conflict in discriminative reward assignment; LLM-jury sidesteps that conflict entirely by using cross-model agreement as the signal. The shared-error floor finding — near zero on math, non-trivial on science — provides a diagnostic for when VLM RL training (which often uses verifiable math/code rewards) can substitute jury verification for trained reward models, and when it cannot.

## My Thoughts

<!-- Add your own notes here -->
