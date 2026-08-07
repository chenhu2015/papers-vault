---
title: "RP-OPSD: Reasoning-Pivot-Guided On-Policy Self-Distillation for Multilingual Reasoning Transfer"
authors: ["Xinye Wang", "Junxiao Liu", "Shujian Huang"]
date: 2026-08-06
arxiv_id: "2608.06347v1"
url: "https://arxiv.org/abs/2608.06347"
score: 0.82
topics: [agentic RL, RLHF, LLM agent]
status: unread
---

# RP-OPSD: Reasoning-Pivot-Guided On-Policy Self-Distillation for Multilingual Reasoning Transfer

## Summary

RP-OPSD identifies 'reasoning pivots' — tokens that advance or redirect the reasoning process — as the most critical targets for OPSD supervision. It uses the distributional shift between matched teacher views (with and without an English reference solution) as a proxy to detect these pivots, concentrating privileged distillation on reasoning-control and state-update tokens while downweighting surface realization tokens. Analysis confirms the method selectively amplifies supervision on the tokens most predictive of cross-lingual reasoning direction, outperforming strong OPSD variants across 17 languages.

## Key Contributions

- Characterizes reasoning pivots as decisions that advance/redirect reasoning and shape subsequent inference (distinct from surface realization tokens)
- Uses distributional shift between matched teacher views (with vs. without English reference solution) as proxy for pivot detection — no external pivot labeling needed
- Concentrates privileged distillation and reference anchoring on reasoning-control and problem-conditioned state-update tokens
- Tested on 17 languages across multiple math difficulty levels; outperforms all strong OPSD baselines

## Relevance

RP-OPSD introduces a token-type axis for OPSD calibration: rather than adapting by temporal position (DASH), temporal persistence (PCSD), confidence-return correlation (ADRS), or scaffold structure (OCSD), it adapts by functional token type (pivot vs. surface). This complements FutureBridge-OPD (state-selection at the step level) with a token-level analogue: FTB asks "which states to supervise," RP-OPSD asks "which token types within a state to prioritize." Together with DASH, this adds two new axes to the Gap #19/20 teacher calibration taxonomy in a single day.

## My Thoughts

<!-- Add your own notes here -->
