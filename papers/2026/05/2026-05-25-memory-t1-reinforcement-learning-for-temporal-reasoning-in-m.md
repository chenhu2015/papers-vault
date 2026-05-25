---
title: "Memory-T1: Reinforcement Learning for Temporal Reasoning in Multi-session Agents"
authors: ["Yiming Du", "Baojun Wang", "Yifan Xiang", "Zhaowei Wang", "Wenyu Huang", "Boyang Xue", "Bin Liang", "Xingshan Zeng", "Fei Mi", "Haoli Bai", "Lifeng Shang", "Jeff Z. Pan", "Yuxin Jiang", "Kam-Fai Wong"]
date: 2026-05-25
arxiv_id: "2512.20092v1"
url: "http://arxiv.org/abs/2512.20092v1"
score: 0.76
topics: [agentic RL, RL training, LLM agent]
status: unread
---

# Memory-T1: Reinforcement Learning for Temporal Reasoning in Multi-session Agents

## Summary

Memory-T1 trains a time-aware memory selection policy using RL for conversational agents that must reason over long multi-session dialogue histories. A coarse-to-fine strategy prunes dialogue history with temporal/relevance filters before an RL agent selects precise evidence sessions, guided by a multi-level reward optimizing answer accuracy, evidence grounding, and temporal consistency (at both session- and utterance-level). A 7B model reaches 67.0% on Time-Dialog, beating a 14B baseline by 10.2% and remaining robust at 128k-token context windows where baselines collapse.

## Key Contributions

- Coarse-to-fine memory selection: temporal/relevance filters prune candidates, RL agent makes fine-grained session selection
- Multi-level reward function with three components: answer accuracy, evidence grounding, and temporal consistency
- Temporal consistency reward provides dense signal at both session-level (chronological proximity) and utterance-level (chronological fidelity)
- Robust to 128k-token dialogue histories where long-context baselines collapse; open-source code and datasets

## Relevance

Complements Memory-R1 (also found today) by targeting the specific challenge of temporal reasoning in long dialogue histories. The RL-trained memory selection policy matches the agentic RL interest and the multi-session agent setting extends the long-horizon RL thread from earlier digests (Milestone-guided, SOLAR-RL, ReBel).

## My Thoughts

<!-- Add your own notes here -->
