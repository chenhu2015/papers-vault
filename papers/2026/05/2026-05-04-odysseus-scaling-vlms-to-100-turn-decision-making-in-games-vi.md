---
title: "Odysseus: Scaling VLMs to 100+ Turn Decision-Making in Games via Reinforcement Learning"
authors: ["Chengshuai Shi", "Wenzhe Li", "Xinran Liang", "Yizhou Lu", "Wenjia Yang", "Ruirong Feng", "Seth Karten", "Ziran Yang", "Zihan Ding", "Gabriel Sarch", "Danqi Chen", "Karthik Narasimhan", "Chi Jin"]
date: 2026-05-01
arxiv_id: "2605.00347v1"
url: "http://arxiv.org/abs/2605.00347v1"
score: 0.85
topics: [multimodal models, vision language models, agentic RL, PPO, RL training]
status: unread
---

# Odysseus: Scaling VLMs to 100+ Turn Decision-Making in Games via Reinforcement Learning

## Summary

Odysseus investigates RL-based training of VLMs for long-horizon decision-making in Super Mario Land, requiring 100+ interaction turns with coordinated perception, reasoning, and action. A systematic ablation shows adapted PPO with a lightweight turn-level critic substantially outperforms critic-free methods (GRPO, Reinforce++) in stability and sample efficiency, while pretrained VLMs provide strong action priors that reduce action engineering overhead. The resulting framework achieves at least 3× average game progress over frontier models and generalises to held-out game levels while preserving general multimodal capabilities.

## Key Contributions

- Systematic comparison of PPO (with turn-level critic) vs. GRPO/Reinforce++ in long-horizon VLM RL — PPO wins convincingly
- Shows pretrained VLMs provide strong action priors, significantly improving sample efficiency over classical deep RL trained from scratch
- Achieves in-game and cross-game generalisation while maintaining general-domain VLM capability (no catastrophic forgetting)
- Releases Odysseus as an open training framework for long-horizon VLM agent training

## Relevance

The vault has covered GUI agents and multi-turn VLM RL (MM-Doc-R1, ERA), but Odysseus directly targets the >100 turn horizon, which is an order of magnitude longer. The finding that adapted PPO with a turn-level critic beats GRPO at long horizons is a direct complement to UCPO's analysis of GRPO's limitations, and adds an architectural answer (critic) to GRPO's diversity/stability problems.

## My Thoughts

<!-- Add your own notes here -->
