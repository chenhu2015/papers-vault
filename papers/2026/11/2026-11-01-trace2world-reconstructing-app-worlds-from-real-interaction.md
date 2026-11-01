---
title: "Trace2World: Reconstructing App Worlds from Real Interaction Traces for Scalable GUI Agent Training"
authors: ["Zezhou Wang", "Hanzhang Zhou", "Panrong Tong", "Quyu Kong", "Pengxiang Li", "Steven Hoi", "Zhuzhong Qian", "Yue Wang"]
date: 2026-11-01
arxiv_id: "2610.30792v1"
url: "https://arxiv.org/abs/2610.30792"
score: 0.78
topics: [agentic RL, RL training, LLM agent, tool use]
status: unread
---

# Trace2World: Reconstructing App Worlds from Real Interaction Traces for Scalable GUI Agent Training

## Summary

Addresses the bottleneck of environment construction for GUI reinforcement learning by reconstructing executable app worlds from real interaction traces, separating behavior inference from implementation. From 1,570 traces it constructs 50 environments with 91.1% end-to-end workflow reproduction (vs. 59.8% for the strongest baseline), and source-grounded validation retains 94% of simulated training gains on real devices. Training in Trace2World improves the model by 20.2 points on its benchmark and 5.4–16.2 points across four external GUI benchmarks.

## Key Contributions

- Separates global behavior reconstruction (shared, source-linked app model) from implementation, avoiding incorrect state transitions from partial traces
- Source-grounded validation: independent replay of source workflows localizes mismatches for bounded implementation repair, retaining 94% of simulated training gains on real devices
- Learner-adaptive task and environment augmentation within source-supported behaviors raises benchmark success from 56.9% to 61.1%
- Scales to 50 executable GUI environments from 1,570 real interaction traces, enabling GUI RL at realistic app diversity

## Relevance

Fills a key infrastructure gap in the GUI agent RL thread (Where to Learn and How Far to Roll Out, Online Dense RL iOS, AndroidFlux): where prior papers focused on training efficiency given environments, Trace2World addresses how to construct those environments from real-world traces rather than synthetic or manually-built ones. Source-grounded validation is a principled answer to the sim-to-real gap that Android/iOS GUI RL papers have implicitly faced.

## My Thoughts

<!-- Add your own notes here -->
