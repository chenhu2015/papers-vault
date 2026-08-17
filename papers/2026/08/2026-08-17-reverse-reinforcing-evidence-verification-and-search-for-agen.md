---
title: "REVERSE: Reinforcing Evidence Verification and Search for Agentic Image Geo-Localization"
authors: ["Yong Li", "Furong Jia", "Dacheng Yin", "Kang Rong", "Fengyun Rao", "Jing Lyu", "Fan Zhang"]
date: 2026-08-17
arxiv_id: "2605.26861v1"
url: "http://arxiv.org/abs/2605.26861v1"
score: 0.74
topics: [multimodal models, vision language models, VLM, agentic RL, reward model]
status: unread
---

# REVERSE: Reinforcing Evidence Verification and Search for Agentic Image Geo-Localization

## Summary

REVERSE teaches three intermediate decisions in multi-turn geo-localization via three distinct process rewards: visual grounding (where to look), query utility (what to query), and evidence discrimination (what evidence to trust). An offline search cache stabilizes retrieval observations during RL, enabling dense process supervision over otherwise noisy search results; a 4B model trained this way rivals substantially larger models on Im2GPS3k and YFCC4k. The three-role process reward decomposition is architecturally distinct from SeekJudge's four-role Seek-Analyze pipeline and occupies a new cell in the multi-step process reward taxonomy: multimodal search-grounded process supervision.

## Key Contributions

- Three-role process reward decomposition: visual grounding, query utility, evidence discrimination (each a distinct reward signal)
- Offline search cache: makes retrieval observations stable and reusable during RL, enabling dense supervision over noisy search
- 4B model rivals much larger baselines; demonstrates process reward effectiveness at small model scale
- Tool-grounded trajectory construction with annotated region selections and geo-informative evidence labels

## Relevance

REVERSE is the first vault paper to apply process rewards to a visually-grounded, retrieval-augmented multi-turn pipeline, extending the VLM process reward thread (SRGPO, SeeNav-Agent) into a search-interactive setting. The offline cache mechanism addresses a practical problem in retrieval-based RL (stochastic search results prevent stable credit assignment) that is analogous to ToolRL-DR's stability concern (transition perturbations) — both identify environmental stochasticity as the core obstacle to dense process supervision and propose a stability mechanism. The visual grounding process reward connects to Gap #7 (visual faithfulness as VLM RL training signal), specifically as an application-specific instantiation where visual grounding reward is a verifiable proxy for visual faithfulness.

## My Thoughts

<!-- Add your own notes here -->
