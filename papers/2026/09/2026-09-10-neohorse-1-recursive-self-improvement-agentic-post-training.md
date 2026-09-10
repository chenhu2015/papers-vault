---
title: "NeoHorse-1: Towards Recursive Self-Improvement via Agentic Post-Training with Routing Harness"
authors: ["NeoHorse Team", "Guoliang Cao", "Guohao Dai", "Tianyu Guo", "Kai Han", "Hailin Hu", "Zihan Jiang", "Xiang Kuang", "Boxun Li", "Yulong Li", "Zehua Pei", "Yuchuan Tian", "Jiamin Wang", "Yu Wang", "Yunhe Wang", "Yihong Wu", "Haiyang Xu", "Shuo Zhang", "Hang Zhou", "Siyang Cheng", "Jiayu Fan", "Wei He", "Qingrui Jiao", "Hongguang Li", "Zhiyuan Li", "Runke Liu", "Xi Liu", "Xinchen Liu", "Sinno Jialin Pan", "Yi Ren", "Liuyang Song", "Chenyu Wang", "Bei Yu", "Quanlu Zhang", "Xiangyu Zhang", "Mengyu Zheng", "Yingjie Zong"]
date: 2026-09-10
arxiv_id: "2609.08183v1"
url: "https://arxiv.org/abs/2609.08183v1"
score: 0.80
topics: [agentic RL, RL training, LLM agent, tool use]
status: unread
---

# NeoHorse-1: Towards Recursive Self-Improvement via Agentic Post-Training with Routing Harness

## Summary

NeoHorse-1 implements recursive self-improvement by combining a heterogeneous model pool with intelligent routing: every user turn records predicted capability demand, selected service tier, and the interaction, which feeds a training pipeline with 6D semantic evaluation and subscene-level labeling. Routing signals organize SFT into a 3-stage curriculum and extend to routing-guided on-policy distillation; capability-guided allocation then converts evaluation feedback into the next training data mixture, closing an evaluation-selection-update loop. Post-training raises macro-average from 58.94→64.87 at 4B and 65.60→69.04 at 9B across eleven agentic and tool-use benchmarks.

## Key Contributions

- **Routing harness for data collection**: records predicted capability demand, selected tier, and interaction for each turn, preserving interleaved reasoning + tool calls + harness context
- **6D semantic evaluation + subscene labeling**: multi-dimensional quality filter for training data admission
- **Routing-guided 3-stage SFT curriculum + on-policy distillation**: routing signals directly structure the training progression
- **Evaluation-selection-update loop**: capability-guided allocation converts benchmark feedback into next training mixture, closing the RSI loop

## Relevance

NeoHorse-1 directly addresses the model-harness compatibility gap surfaced by Co-Evolving Harnesses: it treats the routing harness as an active participant in the training loop — harness signals shape what data is collected, evaluated, and fed back into training. This is the first paper to make harness compatibility an explicit loop signal (as opposed to Co-Evolving Harnesses' per-run on-policy correction). Combined with Experience Funnel's state-policy alternating loop, these three papers (NeoHorse-1, Co-Evolving Harnesses, Experience Funnel) collectively define the emerging space of model-harness co-evolution.

## My Thoughts

<!-- Add your own notes here -->
