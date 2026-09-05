---
title: "SCALECUA: Scaling Computer Use Agents with Verifiable Task Synthesis and Efficient Online RL"
authors: ["Bowen Lv", "Xiao Liu", "Yanyu Ren", "Hanyu Lai", "Bohao Jing", "Hanchen Zhang", "Yanxiao Zhao", "Shuntian Yao", "Jie Tang", "Yuxiao Dong"]
date: 2026-09-05
arxiv_id: "2607.11185v1"
url: "http://arxiv.org/abs/2607.11185v1"
score: 0.76
topics: [agentic RL, LLM agent, multimodal, vision-language, VLM, RL training]
status: unread
---

# SCALECUA: Scaling Computer Use Agents with Verifiable Task Synthesis and Efficient Online RL

## Summary

SCALECUA addresses two bottlenecks in online RLVR for GUI computer-use agents: verifiable data scarcity (solved by VeriGen, which uses iterative docker interactions and a multi-agent feedback loop to produce 24K+ verifiable tasks) and online RL inefficiency (solved by Frontier Sampling, which allocates rollouts to per-task capability frontiers, and Visual Context Segmentation, which provides a 2.83x training speedup over step-wise decomposition). Together, these yield 68.7% on OSWorld and 54.0% on ScienceBoard, state-of-the-art for open-source computer use agents. Frontier Sampling's per-task capability tracking is structurally complementary to HARTS' prefix-sharing rollout efficiency — both address sample efficiency in agentic RL but at different levels (task selection vs. rollout tree structure).

## Key Contributions

- VeriGen: end-to-end framework for generating verifiable RL tasks via iterative docker interactions and a multi-agent feedback loop, producing 24K+ verifiable + 3K high-quality RL tasks
- Frontier Sampling: per-task capability tracking that allocates rollouts to the current learning frontier, avoiding wasted compute on already-solved or unsolvable tasks
- Visual Context Segmentation: sliding window over recent visual context that balances rollout and training-engine pressure, yielding 2.83x speedup over step-wise decomposition
- State-of-the-art open-source computer use: 68.7% OSWorld, 54.0% ScienceBoard

## Relevance

SCALECUA extends the agentic RL efficiency thread (HARTS prefix sharing, GAP dependency-graph parallelization, SINKFLEX-RL training infrastructure) to the data-generation and task-selection levels. Frontier Sampling adds a fifth axis: curriculum-aware rollout allocation — structurally similar to NC-GRPO's diversity pressure (which ensures rollout diversity in latent space) but operating at the task level rather than the trajectory level. VeriGen also demonstrates the scalability of verifiable-reward RL beyond math/code to the full GUI domain.

## My Thoughts

<!-- Add your own notes here -->
