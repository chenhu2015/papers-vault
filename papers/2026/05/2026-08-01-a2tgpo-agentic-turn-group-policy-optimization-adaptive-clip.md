---
title: "A²TGPO: Agentic Turn-Group Policy Optimization with Adaptive Turn-level Clipping"
authors: ["Dingwei Chen", "Zefang Zong", "Zhipeng Ma", "Leo Luo", "Yang Li", "Chengming Li", "Peng Chen", "Jie Jiang"]
date: 2026-05-07
arxiv_id: "2605.06200"
url: "https://arxiv.org/abs/2605.06200"
score: 0.88
topics: [agentic RL, GRPO, LLM agent, tool use]
status: unread
---

# A²TGPO: Agentic Turn-Group Policy Optimization with Adaptive Turn-level Clipping

## Summary

A²TGPO re-designs how Information Gain (IG) is normalized and consumed in agentic turn-level RL by introducing three components: (1) turn-group normalization, which normalizes IG within each (prompt, turn-index) group to prevent positional-context distortion; (2) variance-rescaled discounted accumulation, which divides cumulative IG by √(number of terms) to prevent magnitude drift with trajectory depth; and (3) adaptive turn-level clipping, which widens the PPO clip range for high-IG turns and narrows it for low-IG turns. Directly addresses three systematic challenges that prior IG-based agentic RL work (IGPO, InfoReasoner, InfoPO, CIGPO) identified as open problems in IG normalization and consumption.

## Key Contributions

- **Turn-group normalization**: normalizes each turn's IG against peers at the same interaction depth (same prompt, same turn-index) rather than globally, eliminating positional context distortion across heterogeneous turn positions
- **Variance-rescaled discounted accumulation**: divides accumulated normalized IG by √(number of accumulated terms), keeping advantage magnitudes comparable regardless of trajectory depth
- **Adaptive turn-level clipping**: modulates each turn's PPO clip range based on its normalized IG — high-IG turns get wider update windows, low-IG turns get narrower ones, aligning clipping behavior with informational content
- Closes the three systematic gaps (positional distortion, magnitude drift, fixed clipping) that prior IG-based papers either ignored or treated as limitations

## Relevance

Directly extends the IG-based credit assignment lineage (IGPO Oct 2025 → InfoReasoner Jan 2026 → InfoPO Feb 2026 → CIGPO Jul 2026) characterized across the Jul 28–30 digests, addressing the concrete normalization challenges identified when the lineage was synthesized; the adaptive clipping mechanism also connects to the composability question raised in the Jul 31 digest (whether STARE surprisal and ERPO entropy gating can be combined), since adaptive clipping is a form of information-content-weighted gradient control.

## My Thoughts

<!-- Add your own notes here -->
