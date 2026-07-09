---
title: "DynaWeb: Model-Based Reinforcement Learning of Web Agents"
authors: ["Hang Ding", "Peidong Liu", "Junqiao Wang", "Ziwei Ji", "Meng Cao", "Rongzhao Zhang", "Lynn Ai", "Eric Yang", "Tianyu Shi", "Lei Yu"]
date: 2026-07-09
arxiv_id: "2601.22149v2"
url: "http://arxiv.org/abs/2601.22149v2"
score: 0.78
topics: [agentic RL, LLM agent, tool use, reinforcement learning]
status: unread
---

# DynaWeb: Model-Based Reinforcement Learning of Web Agents

## Summary

DynaWeb is an MBRL framework that trains web agents by first learning a world model that predicts naturalistic web page representations given agent actions, then using that model as a synthetic environment for fast online RL rollouts. Expert trajectories from training data are randomly interleaved with on-policy rollouts to improve stability, and the approach is validated on WebArena and WebVoyager, consistently improving state-of-the-art open-source web agent performance.

## Key Contributions

- Learns a web world model from real browsing trajectories that predicts naturalistic web page representations conditioned on agent actions — enabling fully simulated online RL without live internet interaction
- Agent "dreams" by generating vast rollout trajectories against the world model, enabling fast and safe online policy learning
- Randomly interleaves real expert trajectories with on-policy rollouts during RL training — a practical hybrid that stabilizes world-model-based RL
- Validates the viability of imagination-based web agent training on WebArena and WebVoyager with consistent improvements over base open-source web agents

## Relevance

DynaWeb fills the agentic RL / real-environment gap that has been underrepresented in the vault relative to RLVR theory. It is the web-agent analog of BORA's offline-to-online VLA framework for dexterous manipulation: both use a learned model of the environment to enable RL without direct environment interaction, and both interleave offline expert data with on-policy exploration. The web world model approach is structurally complementary to ARTIST (Jul 09), which uses outcome-based RL with direct environment interaction — together they bracket the model-based vs. model-free spectrum for agentic LLM training.

## My Thoughts

<!-- Add your own notes here -->
