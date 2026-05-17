---
title: "On Training Large Language Models for Long-Horizon Tasks: An Empirical Study of Horizon Length"
authors: ["Sunghwan Kim", "Junhee Cho", "Beong-woo Kwak", "Taeyoon Kwon", "Liang Wang", "Nan Yang", "Xingxing Zhang", "Furu Wei", "Jinyoung Yeo"]
date: 2026-05-04
arxiv_id: "2605.02572"
url: "https://arxiv.org/abs/2605.02572"
score: 0.80
topics: [agentic RL, RL training, LLM agent]
status: unread
---

# On Training Large Language Models for Long-Horizon Tasks: An Empirical Study of Horizon Length

## Summary

This empirical study isolates horizon length as an independent RL training bottleneck for LLM agents: increasing horizon alone induces severe training instability through compounding exploration difficulty and credit assignment challenges, independent of task content. Horizon reduction — training on shorter action subsequences — stabilizes training and generalizes to longer-horizon inference, a phenomenon the authors call horizon generalization. The findings provide a principled empirical basis for designing agentic RL curricula.

## Key Contributions

- Controlled isolation of horizon length as an independent variable in RL training for LLM agents
- Identification of two failure modes induced by long horizons: exploration difficulty and credit assignment degradation
- Horizon reduction principle: shorter training horizons stabilize RL and generalize better to longer inference horizons
- "Horizon generalization" phenomenon: reduced-horizon training models outperform matched-horizon training on longer tasks

## Relevance

Provides direct empirical grounding for curriculum RL design (a thread covered extensively in May 13 digest via METIS/AdaCuRL/VCRL), now approached from the horizon-length angle rather than difficulty scheduling. Connects to the credit assignment thread running through multi-turn agentic RL (May 16) and long-horizon agent work (May 10 milestone-guided paper).

## My Thoughts

<!-- Add your own notes here -->
