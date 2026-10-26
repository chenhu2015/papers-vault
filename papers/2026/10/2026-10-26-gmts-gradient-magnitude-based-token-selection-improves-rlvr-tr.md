---
title: "GMTS: Gradient Magnitude-based Token Selection Improves RLVR Training for LLM Reasoning"
authors: ["Outongyi Lv", "Yuanwei Zhang", "Xiaoqun Zhang"]
date: 2026-08-31
arxiv_id: "2608.30632v1"
url: "http://arxiv.org/abs/2608.30632v1"
score: 0.82
topics: [RLHF, GRPO, reward model, RL training, reinforcement learning]
status: unread
---

# GMTS: Gradient Magnitude-based Token Selection Improves RLVR Training for LLM Reasoning

## Summary

GMTS challenges entropy-based token selection by showing that while high-entropy tokens correlate with large gradients within a single answer, entropy fails to reflect token importance across answers with varying reward signals. By leveraging the entropy-gradient connection to approximate gradient-magnitude rankings, GMTS selects the top 20% tokens by estimated gradient magnitude, consistently outperforming entropy-based selection across three reasoning domains and multiple model sizes. This provides a more principled fine-grained token contribution estimate for RLVR training.

## Key Contributions

- Identifies a fundamental flaw in entropy-based token selection: answer-level reward variation breaks the entropy-gradient correlation across answers
- GMTS uses the within-answer entropy-gradient connection to approximate cross-answer gradient magnitudes without computing actual gradients
- Top 20% GMTS-selected tokens outperform entropy selection consistently across 3 reasoning domains and multiple model sizes
- Frames token selection as a credit assignment problem at the token level within RLVR

## Relevance

GMTS directly addresses token-level credit assignment within RLVR, complementing the step-credit cluster (SCOPE-RL, ReAPO) with a finer-grained intra-trajectory perspective. The key insight — that answer-level reward variation breaks entropy as a cross-answer proxy — is a principled critique of the entropy-selection approach used in several prior RLVR papers and opens a new angle on efficient RLVR training.

## My Thoughts

<!-- Add your own notes here -->
