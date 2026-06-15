---
title: "LiteCoder-Terminal: Scaling Long-Horizon Terminal Environments for Learning Language Agents"
authors: ["Xiaoxuan Peng", "Kaiqi Zhang", "Xinyu Lu", "Boxi Cao", "Yaojie Lu", "Hongyu Lin", "Xianpei Han", "Le Sun"]
date: 2026-05-28
arxiv_id: "2605.29559v1"
url: "https://arxiv.org/abs/2605.29559"
score: 0.74
topics: [agentic RL, RL training, LLM agent]
status: unread
---

# LiteCoder-Terminal: Scaling Long-Horizon Terminal Environments for Learning Language Agents

## Summary

LiteCoder-Terminal-Gen is a zero-dependency pipeline that synthesizes executable, verifiable terminal training environments from domain specifications, producing 11K SFT expert trajectories and 602 RL environments for Direct Multi-turn Preference Optimization (DMPO). The approach shows that fully synthetic terminal environments provide a scalable and verifiable supervision signal: SFT provides the main capability jump while DMPO adds targeted gains on macro recall. A Qwen-32B model trained on this data achieves 29.06%/18.54%/34.00% pass@1 across TerminalBench 1.0/2.0/Pro.

## Key Contributions

- Zero-dependency environment synthesis requiring only domain specifications — no scraped external repositories
- Dual-dataset construction: SFT expert trajectories + RL verifiable environments from the same synthesis pipeline
- DMPO (Direct Multi-turn Preference Optimization): trajectory-level preference optimization over multi-turn interactions
- Demonstrates SFT→DMPO pipeline for terminal/command-line agentic capability at scale

## Relevance

Establishes a third data point in the synthetic environment synthesis pattern alongside CUA-Gym (Jun 13, RLVR for computer-use agents) and FORT-Searcher (Jun 11, shortcut-resistant search data): synthetic verifiable environment generation is the key scalability bottleneck for agentic RL across domains, and zero-dependency synthesis pipelines are the emerging solution.

## My Thoughts

<!-- Add your own notes here -->
