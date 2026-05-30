---
title: "Grounding the Score: Explicit Visual Premise Verification for Reliable Vision-Language Process Reward Models"
authors: ["Junxin Wang", "Dai Guan", "Weijie Qiu", "Zhihang Li", "Yongbo Gai", "Zhengyi Yang", "Mengyu Zhou", "Erchao Zhao", "Xiaoxi Jiang", "Guanjun Jiang"]
date: 2026-03-17
arxiv_id: "2603.16253"
url: "http://arxiv.org/abs/2603.16253v2"
score: 0.78
topics: [VLM, vision-language, reward model, multimodal]
status: unread
---

# Grounding the Score: Explicit Visual Premise Verification for Reliable Vision-Language Process Reward Models

## Summary

EVPV decouples perceptual uncertainty from logical evaluation in VL process reward models by prompting the policy to produce a step-wise visual checklist, deriving structured visual constraints from the image independently, then calibrating PRM step rewards via reliability gating — preserving rewards when visual evidence is reliable, attenuating when it is not. On VisualProcessBench and six multimodal reasoning benchmarks, EVPV consistently boosts Best-of-N reranking accuracy over strong baselines.

## Key Contributions

- Step-wise visual checklist makes required visual facts explicit per reasoning step
- Independent visual constraint extractor derives structured claims from the image
- Reliability gating: reward attenuation when checklist-constraint agreement is low
- Controlled corruption experiments confirm gains are causally from constraint fidelity, not prompt effects

## Relevance

Addresses the visual perception-reasoning entanglement in VL-PRMs — a complementary approach to MIRL (found today) from a process reward model perspective rather than sampling budget allocation.

## My Thoughts

<!-- Add your own notes here -->
