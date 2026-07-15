---
title: "LLMs as a Jury: Cross-Model Consensus Can Outperform Process Reward Models for LLM Reasoning"
authors: ["Ning Liu"]
date: 2026-07-15
arxiv_id: "2607.10139"
url: "http://arxiv.org/abs/2607.10139v1"
score: 0.82
topics: [reward model, RL training, RLAIF, agentic RL]
status: unread
---

# LLMs as a Jury: Cross-Model Consensus Can Outperform Process Reward Models for LLM Reasoning

## Summary

Cross-model consensus — using agreement across independently trained models each solving a problem once — outperforms self-consistency and trained PRMs for answer selection, closing the entire gap to an oracle selector on competition math. The mechanism is error decorrelation: independent models err differently so wrong answers scatter while correct ones accumulate agreement. Derives a closed-form parameter-free law predicting consensus accuracy from three panel statistics, exposing a shared-error floor where models share misconceptions.

## Key Contributions

- Cross-model consensus (LLM-jury) beats self-consistency and matches/outperforms trained PRMs (discriminative, ORM, GenRM) on 7 math benchmarks inside training domain; top selector outside it
- Error decorrelation mechanism: independently trained models have uncorrelated errors, so agreement accumulates at correct answers
- Closed-form parameter-free law predicting consensus accuracy from three panel statistics (allows predicting when to trust the jury in advance)
- Identifies shared-error floor: near zero on math, non-trivial on science — exposes where jury consensus fails (shared misconceptions)

## Relevance

Directly challenges the vault's PRM thread (GroundedPRM, HRM, KV-PRM) with a no-cost alternative: if diverse independent models are available (as in multi-agent settings), consensus can match expensive trained PRMs without any PRM training data. The shared-error floor finding also connects to the DISA/ARMOR thread on diversity collapse in GRPO — both identify homogenization of model outputs (whether from over-optimization or shared misconceptions) as the failure mode. KV-PRM's O(L) scoring efficiency is most valuable where jury consensus fails (science with shared misconceptions).

## My Thoughts

<!-- Add your own notes here -->
