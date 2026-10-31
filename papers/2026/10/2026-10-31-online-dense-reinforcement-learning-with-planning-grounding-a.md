---
title: "Online Dense Reinforcement Learning with Planning-Grounding Agent for UI Navigation on Live IOS Apps"
authors: ["Peitong Duan", "Khashayar Gatmiry", "Jeffrey Nichols", "Samy Bengio", "Emmanuel Abbe"]
date: 2026-10-31
arxiv_id: "2610.39264v1"
url: "http://arxiv.org/abs/2610.39264v1"
score: 0.85
topics: [agentic RL, multimodal models, vision language models, VLM, LLM agent, tool use]
status: unread
---

# Online Dense Reinforcement Learning with Planning-Grounding Agent for UI Navigation on Live IOS Apps

## Summary

Online RL framework trains smaller VLM UI navigation agents directly on live iOS apps by decoupling a Planning LLM from a UI Grounding model, using PPO with step-level advantage estimation and a novel GiGPPO critic that stabilises value estimation via reward signals from visually similar states across concurrent trajectories. LLM-as-Judge provides both dense step-level and terminal rewards; infrastructure orchestrates hundreds of concurrent virtual iOS devices at scale. The 8B RL agent achieves nearly 7x OOD generalization to Android and matches Gemini-3.1-Pro on real iOS applications.

## Key Contributions

- Decoupled Planning + UI Grounding architecture for online RL in live iOS apps (avoids brittleness of monolithic SFT models)
- GiGPPO: neighbor-conditioned value estimation using reward signals from visually similar states in concurrent trajectories — stabilises critic under sparse GUI feedback
- Dual reward: LLM-as-Judge provides dense step-level progress reward + terminal task completion reward
- 7x OOD generalization to Android from iOS training; matches Gemini-3.1-Pro on real iOS apps at 8B scale

## Relevance

Directly follows the GUI agent / computer use RL thread opened by MAI-Gym (Oct 30). Unlike MAI-Gym which was an RL platform, this paper delivers a complete online-RL training system with a novel critic (GiGPPO) that solves a concrete problem — critic instability in GUI agents — analogous to how FOCUS's selective branching solves critic instability in text agents. The dense step reward via LLM-as-Judge is complementary to the VLM RL reward design work in PerceptRL and CoFire.

## My Thoughts

<!-- Add your own notes here -->
