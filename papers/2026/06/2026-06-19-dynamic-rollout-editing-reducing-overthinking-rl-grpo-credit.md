---
title: "Dynamic Rollout Editing for Reducing Overthinking in RL-Trained Reasoning Models"
authors: ["Zihao Wei", "Wenjie Shi", "Liang Pang", "Jingcheng Deng", "Shicheng Xu", "Shasha Guo", "Zenghao Duan", "Jiahao Liu", "Jingang Wang", "Huawei Shen", "Xueqi Cheng"]
date: 2026-06-19
arxiv_id: "2606.17890v1"
url: "http://arxiv.org/abs/2606.17890v1"
score: 0.81
topics: [GRPO, RL training, credit assignment, reward model, PPO]
status: unread
---

# Dynamic Rollout Editing for Reducing Overthinking in RL-Trained Reasoning Models

## Summary

GRPO assigns sequence-level credit, so successful trajectories that continue generating after the correct answer emerges receive positive signal for their unnecessary tail — framing overthinking as a training-time credit-assignment failure rather than a decoding-time stopping problem. Dynamic Rollout Editing (DRE) preserves the verified answer-reaching prefix of successful trajectories, edits out the unnecessary continuation, and biases the RL group preference toward the edited version, weakening reinforcement of unnecessary thinking without penalizing the reasoning that reached the answer. DRE consistently reduces overthinking across diverse tasks.

## Key Contributions

- Diagnoses overthinking as a GRPO credit-assignment failure: early-training rollouts show successful trajectories slightly overthink more than unsuccessful ones for the same prompt, seeding a feedback loop that GRPO amplifies
- DRE preserves the verified correct prefix and edits the unnecessary continuation in successful trajectories, then uses the edited trajectory as the preferred alternative within the same RL group
- Weakens positive update signal for unnecessary thinking without introducing a negative penalty for the reasoning needed to reach the answer
- Demonstrates effectiveness across diverse tasks without architecture changes or additional supervision

## Relevance

Provides a fourth angle on the credit assignment thread: AT-RL (Jun 14) assigns credit to high-anchor tokens within a step, HiMPO (Jun 18) assigns credit to memory-writing actions, RODS (Jun 18) selects data at the capability boundary. DRE identifies a credit mis-assignment at the trajectory level — GRPO cannot distinguish the good prefix from the unnecessary suffix in a successful trajectory, and DRE surgically corrects this by editing before the RL update rather than filtering after. The sequence-level credit limitation it exposes is a fundamental constraint of GRPO's group-relative design.

## My Thoughts

<!-- Add your own notes here -->
