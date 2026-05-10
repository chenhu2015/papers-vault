---
title: "A Subgoal-driven Framework for Improving Long-Horizon LLM Agents"
authors: ["Taiyi Wang", "Sian Gooding", "Florian Hartmann", "Oriana Riva", "Edward Grefenstette"]
date: 2026-03-20
arxiv_id: "2603.19685"
url: "http://arxiv.org/abs/2603.19685v1"
score: 0.85
topics: [agentic RL, RL training, LLM agent, reward model]
status: unread
---

# A Subgoal-driven Framework for Improving Long-Horizon LLM Agents

## Summary

MiRA introduces milestone-based dense reward signals for RL fine-tuning of web navigation agents, decomposing long-horizon tasks into subgoals to eliminate the sparse/delayed reward bottleneck that stalls standard RL on multi-step environments. Applied to Gemma3-12B, MiRA lifts success rate from 6.4% to 43.0% on WebArena-Lite, surpassing GPT-4-Turbo (17.6%), GPT-4o (13.9%), and the previous open-model SOTA WebRL (38.4%).

## Key Contributions

- Identifies two failure modes: agents losing track of the goal during online execution, and sparse rewards degrading RL fine-tuning
- Subgoal decomposition framework using proprietary models for online planning (+~10% absolute SR on WebArena-Lite)
- MiRA: milestone-based dense reward signals for RL training on web navigation
- Gemma3-12B: 6.4%→43.0% on WebArena-Lite, beating GPT-4-Turbo and prior open-source SOTA

## Relevance

Strong result on the web navigation RL problem — directly relevant to agentic RL and the long-horizon credit assignment thread opened by BEACON today. The huge gap between baseline (6.4%) and MiRA (43%) underlines the severity of sparse rewards in realistic agentic settings, motivating both this and the BEACON/HCAPO papers in today's digest.

## My Thoughts

<!-- Add your own notes here -->
