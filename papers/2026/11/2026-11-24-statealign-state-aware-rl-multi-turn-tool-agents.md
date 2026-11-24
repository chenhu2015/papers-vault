---
title: "StateAlign: Internalizing State-Aware Decision-Making for Reliable Multi-Turn Tool Agents via Reinforcement Learning"
authors: ["Zhexi Lu", "Subhajit Chaudhury", "Tejaswini Pedapati", "Keerthiram Murugesan", "Lei Yu"]
date: 2026-11-24
arxiv_id: "2611.16304v1"
url: "http://arxiv.org/abs/2611.16304v1"
score: 0.75
topics: [agentic RL, RL training, tool use]
status: unread
---

# StateAlign: Internalizing State-Aware Decision-Making for Reliable Multi-Turn Tool Agents via Reinforcement Learning

## Summary

Addresses the tension between task accuracy and tool hallucination in RL-trained multi-turn tool agents: agents sometimes execute calls when they should seek information, retrieve data, or decline infeasible requests — even when their own reasoning identifies the missing information. Introduces StateAlign, combining task-state construction covering five task conditions (available info, tool capabilities, task progress variants) with state-contrastive RL that applies token-level contrasts between paired states; outcome rewards guide task completion while contrastive signals train outputs that fit the current state.

## Key Contributions

- Identifies state-misaligned decisions as a failure mode distinct from general task failure (tool hallucination persists even with high accuracy)
- Task-state construction: five conditions paired with differing action requirements for contrastive training signal
- State-contrastive RL: token-level comparison of reasoning/actions under paired states, not just outcome-level comparison
- Qwen3-8B: BFCL v4 multi-turn accuracy 45.5% → 55.2%; no-tool hallucination 62.2% → 56.1% on SimpleToolHalluBench

## Relevance

Directly on the tool use RL training thread. Complements TACA (which addresses credit assignment failure) by targeting a different failure mode: decision misalignment with task state rather than gradient corruption. Together these address two distinct ways RL training degrades tool-use agents.

## My Thoughts

<!-- Add your own notes here -->
