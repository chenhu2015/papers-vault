---
title: "Segmenting Text and Learning Their Rewards for Improved RLHF in Language Model"
authors: ["Yueqin Yin", "Shentao Yang", "Yujia Xie", "Ziyi Yang", "Yuting Sun", "Hany Awadalla", "Weizhu Chen", "Mingyuan Zhou"]
date: 2026-07-07
arxiv_id: "2501.02790v1"
url: "http://arxiv.org/abs/2501.02790v1"
score: 0.75
topics: [RLHF, reward model, reinforcement learning, LLM agent]
status: unread
---

# Segmenting Text and Learning Their Rewards for Improved RLHF in Language Model

## Summary

This paper addresses the granularity gap between sparse bandit RLHF (response-level reward) and overly subtle token-level RLHF by training a segment-level reward model that assigns reward to each semantically complete text segment spanning a short token sequence. The method supports dynamic text segmentation compatible with standard sequence-preference datasets and generalizes scalar bandit normalizers into location-aware normalizer functions for proper dense reward assignment. It performs competitively on AlpacaEval 2.0, Arena-Hard, and MT-Bench.

## Key Contributions

- Segment-level reward model bridging response-level (bandit) and token-level granularity for RLHF
- Dynamic text segmentation: no fixed segment boundaries, compatible with standard preference datasets
- Location-aware normalizer functions: extends scalar bandit reward normalizers to handle segment position
- Segment reward interpolation for further densification toward token-level signal

## Relevance

Fills a slot in the reward granularity hierarchy being built in the vault. The Jul 6 sentence-level reward model (differential boundary + attention aggregation) operates at sentence boundaries and trains against Bradley-Terry directly; this paper operates at semantically-defined segment boundaries and integrates with the standard RLHF training loop via location-aware normalizers. Together they represent two independent implementations of sub-response-level RLHF: one structural (sentence boundary), one semantic (segment boundary defined by content), forming a complementary pair for the RLHF thread.

## My Thoughts

<!-- Add your own notes here -->
