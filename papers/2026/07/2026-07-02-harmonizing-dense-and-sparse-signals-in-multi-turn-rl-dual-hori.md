---
title: "Harmonizing Dense and Sparse Signals in Multi-turn RL: Dual-Horizon Credit Assignment for Industrial Sales Agents"
authors: ["Haojin Yang", "Ai Jian", "Xinyue Huang", "Yiwei Wang", "Weipeng Zhang", "Ke Zeng", "Xunliang Cai", "Jingqing Ruan"]
date: 2026-07-02
arxiv_id: "2603.01481v1"
url: "https://arxiv.org/abs/2603.01481"
score: 0.75
topics: [agentic RL, GRPO, reward model, LLM agent, multi-step]
status: unread
---

# Harmonizing Dense and Sparse Signals in Multi-turn RL: Dual-Horizon Credit Assignment for Industrial Sales Agents

## Summary

DuCA (Dual-Horizon Credit Assignment) disentangles turn-level (fluency, compliance) and session-level (conversion rate) reward optimization in multi-turn GRPO by separately normalizing their advantages before fusion via HIAN (Horizon-Independent Advantage Normalization), preventing high-magnitude session rewards from overwhelming fine-grained turn-level signals. Applied to a conversational sales agent, DuCA achieves +6.82% relative improvement in conversion rate, 82.28% reduction in inter-sentence repetition, and 27.35% lower identity detection rate versus GRPO baseline.

## Key Contributions

- DuCA framework disentangling optimization across temporal scales in multi-turn conversational RL
- HIAN: Horizon-Independent Advantage Normalization separately normalizes turn-level and session-level advantage estimates before gradient fusion
- Prevents dominant session-level reward signal from suppressing turn-level linguistic quality signals
- Validated on industrial conversational sales with high-fidelity user simulator; addresses domain with non-verifiable session-level outcomes

## Relevance

DuCA operationalizes the multi-timescale credit problem that PASS (Jul 1) diagnosed at the signal layer: where PASS addresses channel contamination between process and outcome signals stacked on a single token stream, DuCA separates normalization across two temporal horizons before any fusion. This is the same structural insight applied at the episode time scale rather than the token time scale. DuCA also provides the first concrete evaluation of GRPO for genuinely non-verifiable multi-turn tasks (sales conversion is soft and lagged), directly complementing GOLF and the open-ended task thread from Jun 30.

## My Thoughts

<!-- Add your own notes here -->
