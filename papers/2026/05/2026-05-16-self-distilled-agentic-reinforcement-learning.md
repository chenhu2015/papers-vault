---
title: "Self-Distilled Agentic Reinforcement Learning"
authors: ["Zhengxi Lu", "Zhiyuan Yao", "Zhuowen Han", "Zi-Han Wang", "Jinyang Wu", "Qi Gu", "Xunliang Cai", "Weiming Lu", "Jun Xiao", "Yueting Zhuang", "Yongliang Shen"]
date: 2026-05-16
arxiv_id: "2605.15155v1"
url: "http://arxiv.org/abs/2605.15155v1"
score: 0.86
topics: [agentic RL, LLM agent, RL training, RLAIF, reinforcement learning]
status: unread
---

# Self-Distilled Agentic Reinforcement Learning

## Summary

SDAR treats on-policy self-distillation (OPSD) from a teacher branch with privileged context as a gated auxiliary objective while keeping RL as the primary backbone, resolving the instability of naive GRPO+OPSD in multi-turn agents. A sigmoid gate over detached token-level signals strengthens distillation on teacher-endorsed positive-gap tokens and softly attenuates negative rejections, yielding +9.4% on ALFWorld, +7.0% on Search-QA, and +10.2% on WebShop over GRPO across Qwen2.5 and Qwen3.

## Key Contributions

- Identifies why OPSD fails when naively combined with RL in multi-turn agents: compounding instability from multi-turn dynamics and skill-conditioned negative rejections
- SDAR: sigmoid gating maps detached token-level distillation signals into a multiplicative gate, selectively preserving and attenuating teacher guidance
- RL remains primary optimization; OPSD acts as auxiliary — avoids the instability of making OPSD the primary signal
- +9.4% ALFWorld, +7.0% Search-QA, +10.2% WebShop; consistent across Qwen2.5 and Qwen3 families

## Relevance

Bridges the self-play/self-improvement thread from May 15 (SPIRAL, SeRL, SPELL) with the multi-turn agentic RL thread explored today. SDAR uses a different form of "AI-generated supervision" (privileged teacher context) than pure self-play, but the gating mechanism is a useful contrast to how May 15's SeRL uses majority-vote self-rewarding. Together these papers form a coherent cluster on how to extract structured learning signal without external annotation in multi-turn settings.

## My Thoughts

<!-- Add your own notes here -->
