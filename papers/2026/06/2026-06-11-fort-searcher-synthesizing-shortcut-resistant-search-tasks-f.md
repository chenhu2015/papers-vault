---
title: "FORT-Searcher: Synthesizing Shortcut-Resistant Search Tasks for Training Deep Search Agents"
authors: ["Jia Deng", "Yimeng Chen", "Xiaoqing Xiang", "Ziyang Zeng", "Shuo Tang", "Wayne Xin Zhao", "Feng Chang", "Chuan Hao", "Yuan Wei", "Ran Tao", "Bryan Dai", "Ji-Rong Wen"]
date: 2026-06-11
arxiv_id: "2606.12087v1"
url: "http://arxiv.org/abs/2606.12087v1"
score: 0.82
topics: [agentic RL, tool use, LLM agent, agentic]
status: unread
---

# FORT-Searcher: Synthesizing Shortcut-Resistant Search Tasks for Training Deep Search Agents

## Summary

Training data for deep search agents commonly contains shortcuts — cheaper identifying routes that allow models to bypass the intended multi-step search — which structural complexity metrics miss entirely. FORT formalizes four actionable shortcut risk types and uses trajectory signature diagnostics (solving cost, answer hit time, prior-shortcut rate) to measure their realized effects, then synthesizes shortcut-resistant training data by controlling all four risks across entity selection, graph construction, question formulation, and adversarial refinement. FORT-Searcher trained with SFT-only on the resulting data achieves the best overall performance among comparable-size open-source search agents on challenging deep search benchmarks.

## Key Contributions

- Shortcut-aware difficulty framework with 4 risk types: evidence co-coverage, single-clue selectivity, exposed constants, prior-knowledge binding
- Trajectory signature diagnostics: solving cost, answer hit time, prior-shortcut rate to measure realized shortcut use
- FORT synthesis pipeline controls risks at entity selection, graph construction, question formulation, and adversarial refinement stages
- SFT-only FORT-Searcher achieves best among comparable open-source search agents; implies data quality bottleneck, not algorithm

## Relevance

Directly follows the Search Agent Training Study thread flagged in the Jun 10 digest. The striking finding — SFT-only beats RL-trained agents when data is shortcut-resistant — complements query recycling and TRACE from the same digest: all three expose a training data quality / distribution mismatch as the core bottleneck in search agent RL.

## My Thoughts

<!-- Add your own notes here -->
