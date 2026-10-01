---
title: "A Self-Supervised Reinforcement Learning Approach for Fine-Tuning Large Language Models Using Cross-Attention Signals"
authors: ["Unknown"]
date: 2026-10-01
arxiv_id: "2502.10482v2"
url: "http://arxiv.org/abs/2502.10482v2"
score: 0.76
topics: [reinforcement learning, RL training, RLHF, reward model]
status: unread
---

# A Self-Supervised Reinforcement Learning Approach for Fine-Tuning Large Language Models Using Cross-Attention Signals

## Summary

This paper uses the model's own cross-attention patterns as a self-supervised reward signal for LLM post-training, extracting measures of prompt coverage, focus, and coherence from attention weights during generation. These intrinsic signals rank candidate responses and guide iterative policy fine-tuning without human labels or a separate reward model. The approach occupies a distinct position from cycle-consistency (CCS) in the no-gold-labels design space: where CCS uses output reconstructability as a proxy, this work uses internal attention fidelity to the input.

## Key Contributions

- Intrinsic reward from cross-attention: extracts prompt coverage, focus, and coherence measures from attention weights, turning internal model signals into a self-supervised reward
- No external supervision required: reward derives entirely from the model's own generative process, enabling post-training without human annotations or a separate reward model
- Iterative fine-tuning loop: ranks candidates by attention-derived reward, updates the policy, repeats — a self-improving cycle without external feedback
- New point in the no-gold-labels reward design space: complements CCS (output-side cycle consistency) with an input-side attention fidelity signal

## Relevance

Directly advances the "no gold labels" thread opened by CCS (2026-09-30). Where CCS provides a reward proxy based on cycle-consistency of outputs, this paper provides a complementary proxy based on internal attention alignment to the input. Together they suggest a design space of intrinsic reward signals: reconstructability (CCS), attention fidelity (this paper), and process consistency — all avoiding the fluency confound critique raised by "Credit Without Ground Truth" (2026-09-28).

## My Thoughts

<!-- Add your own notes here -->
