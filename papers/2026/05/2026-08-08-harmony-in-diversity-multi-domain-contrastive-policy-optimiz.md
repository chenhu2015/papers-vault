---
title: "Harmony in Diversity: Multi-domain Contrastive Policy Optimization for Large Reasoning Models"
authors: ["Zongji Yu", "Wenshui Luo", "Yiliu Sun", "Hao Fang", "Runmin Cong", "Chaochao Lu", "Chen Gong"]
date: 2026-08-08
arxiv_id: "2605.25443v1"
url: "http://arxiv.org/abs/2605.25443v1"
score: 0.75
topics: [GRPO, RL training, agentic RL]
status: unread
---

# Harmony in Diversity: Multi-domain Contrastive Policy Optimization for Large Reasoning Models

## Summary

MCPO addresses cross-domain interference in multi-domain GRPO-style RL through contrastive learning: for a given prompt, transferable reasoning trajectories from other domains serve as positives while incorrect rollouts serve as negatives, promoting knowledge sharing rather than mere interference suppression. Intra-domain correct rollouts are aligned into a consolidated representation space. MCPO outperforms single-domain training in several benchmarks, showing contrastive cross-domain structure can convert harmful interference into beneficial transfer.

## Key Contributions

- Contrastive framing: cross-domain transferable trajectories as positives, incorrect rollouts as negatives
- Promotes knowledge sharing across domains rather than pure interference avoidance
- Intra-domain alignment step consolidates correct rollout representations
- Outperforms single-domain training in some cases, showing cross-domain contrastive structure is beneficial

## Relevance

MCPO provides a contrastive counterpart to the decoupling approaches in the multi-task RL thread (Switch-Reasoner's dual-level mode balance, SFT Conflicts/RL Coexists Parallel-RL). Where those methods separate global balance from local update decisions, MCPO reframes the relationship between domains as a contrastive learning problem — explicitly identifying which cross-domain trajectories are transferable rather than treating all cross-domain signal as interference to suppress. This is a structurally different approach: instead of decoupling, it couples domains through contrastive alignment. The positive/negative trajectory classification is also reminiscent of the GRPO all-fail filtering literature (Gap #16), but operates across domains rather than within a single group.

## My Thoughts

<!-- Add your own notes here -->
