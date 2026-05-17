---
title: "Context Training with Active Information Seeking"
authors: ["Zeyu Huang", "Adhiguna Kuncoro", "Qixuan Feng", "Jiajun Shen", "Lucio Dery", "Arthur Szlam", "Marc'Aurelio Ranzato"]
date: 2026-05-13
arxiv_id: "2605.13050"
url: "https://arxiv.org/abs/2605.13050"
score: 0.70
topics: [tool use, LLM agent, agentic]
status: unread
---

# Context Training with Active Information Seeking

## Summary

This work equips LLM context optimizers with Wikipedia search and browser tools for active information seeking, finding that naively adding tools to sequential context optimization degrades performance but that a search-based training procedure maintaining and pruning multiple candidate contexts delivers consistent, substantial gains. The method is training-free for the LLM itself (no weight updates), data-efficient, and produces contexts that generalize across model families. Evaluated on low-resource translation, health scenarios, and reasoning-heavy benchmarks.

## Key Contributions

- Shows naive tool addition to context optimization pipelines degrades performance vs. baselines
- Search-based training procedure: maintains beam of candidate contexts, uses search/browser tools to refine them
- Pruning strategy over multiple candidate contexts captures complementary information from active retrieval
- Training-free for the LLM; generated contexts transfer across different model architectures

## Relevance

Connects to the "tool use" core keyword through a retrieval-augmented in-context learning angle — distinct from the RL-based tool-use training covered in May 16 (CM2, multi-turn iterative reward calibration) in that it optimizes context rather than training the model to use tools via rewards.

## My Thoughts

<!-- Add your own notes here -->
