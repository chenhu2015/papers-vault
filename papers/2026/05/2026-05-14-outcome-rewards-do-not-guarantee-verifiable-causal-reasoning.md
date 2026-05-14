---
title: "Outcome Rewards Do Not Guarantee Verifiable or Causally Important Reasoning"
authors: ["Qinan Yu", "Alexa Tartaglini", "Peter Hase", "Carlos Guestrin", "Christopher Potts"]
date: 2026-05-14
arxiv_id: "2604.22074"
url: "https://arxiv.org/abs/2604.22074"
score: 0.85
topics: [RLHF, RLAIF, reward model, RL training, agentic RL]
status: unread
---

# Outcome Rewards Do Not Guarantee Verifiable or Causally Important Reasoning

## Summary

RLVR improves task accuracy but does not reliably improve whether the reasoning chain causally drives the final answer, as shown via two new metrics: Causal Importance of Reasoning (CIR) and Sufficiency of Reasoning (SR). Experiments on Qwen2.5 across ReasoningGym tasks reveal that RL optimises output correctness while leaving reasoning chains causally disconnected; joint CIR/SR auxiliary rewards on top of the outcome reward fix both without sacrificing accuracy, and a small SFT warm-up also helps.

## Key Contributions

- CIR (Causal Importance of Reasoning): measures cumulative effect of reasoning tokens on the final answer via counterfactual masking
- SR (Sufficiency of Reasoning): measures whether a verifier can resolve the answer from the reasoning chain alone
- Empirical finding: RLVR trains models to get correct answers without grounding the reasoning causally
- Fix: auxiliary CIR/SR rewards on top of outcome reward matches accuracy while restoring causal reasoning

## Relevance

Connects to the reward hacking / Goodhart's Law thread (May 11) and the RLVR theory work (Binary Rewards from May 11, Alignment Collapse from May 12). This is an important diagnostic paper that questions whether standard RLVR pipelines actually produce what practitioners assume — reasoning that matters.

## My Thoughts

<!-- Add your own notes here -->
