---
title: "SHARPO: Segment-Level Credit Assignment for Agentic Reinforcement Learning"
authors: ["Xinchen Du", "Zhengze Zhou", "Wenhui Zhu", "Han Yu", "Sen Na", "Rohit Jain", "Alborz Geramifard"]
date: 2026-09-30
arxiv_id: "2610.00838"
url: "https://arxiv.org/abs/2610.00838"
score: 0.85
topics: [agentic RL, RL training, GRPO]
status: unread
---

# SHARPO: Segment-Level Credit Assignment for Agentic Reinforcement Learning

## Summary

SHARPO refines GRPO at the level of environment-facing segments by computing teacher-student log-probability gaps within each segment and deriving a bounded advantage multiplier from the gap signal. The multiplier is shared across all tokens within a segment, allowing credit to vary at segment granularity while remaining coarser than per-token assignment — a deliberate middle ground between trajectory-level GRPO and fully token-level methods. Outperforms GRPO, SDAR, RLSD, and StepOPSD on ALFWorld and WebShop with Qwen2.5-7B-Instruct.

## Key Contributions

- Defines segments as environment-facing action units (between environment interactions) as the credit granularity level
- Teacher-student log-probability gap within a segment quantifies how much the segment deviates from ideal behavior
- Bounded multiplier on GRPO advantage prevents instability; shared within segment preserves token-level coherence
- Inspired by OPSD but operates at segment level rather than token level — explicitly a middle-ground design choice

## Relevance

Occupies a new position in the step-credit design space: between GRPO (trajectory-level) and fully token-level methods (TASPO, TPAE). Connects to TASPO's supervision-credit gap formalization — SHARPO's segment boundary is another answer to "at what granularity should credit vary?" FAULT and ProVer target single pivotal segments; SHARPO applies a continuous multiplier across all segments simultaneously. These three papers together define a spectrum of segment-targeting strategies released within two days of each other.

## My Thoughts

<!-- Add your own notes here -->
