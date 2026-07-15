---
title: "Visually Grounded Self-Reflection for Vision-Language Models via Reinforcement Learning"
authors: ["Liyan Tang", "Fangcong Yin", "Greg Durrett"]
date: 2026-07-15
arxiv_id: "2607.02490"
url: "http://arxiv.org/abs/2607.02490v1"
score: 0.83
topics: [multimodal models, VLM, vision language models, RL training, agentic RL]
status: unread
---

# Visually Grounded Self-Reflection for Vision-Language Models via Reinforcement Learning

## Summary

VRRL proposes trajectory prefix masking (to emphasize recovery from errors over avoiding early mistakes) and buffered roll-ins from an experience replay buffer to expose VLMs to diverse failure states during RL training. The method substantially improves OOD accuracy on visual grounding tasks (tables, charts, spatial navigation) where standard RL and reflection fine-tuning degrade significantly under distribution shift. Trajectory prefix masking plus experience replay is the VLM analog of RSPO's reward-swap insight: restructuring the training distribution to better cover recovery behavior.

## Key Contributions

- Trajectory prefix masking: randomly masks trajectory prefixes during RL training so the model must learn to recover from mid-trajectory errors, not just avoid them
- Experience replay buffer: stores diverse failure states from prior rollouts, exposing model to distribution of failures broader than current policy generates
- Substantially improves OOD accuracy on visual grounding (tables, charts, spatial navigation) where standard RL and reflection fine-tuning degrade
- Frames VLM self-reflection as a distribution coverage problem: standard RL only trains on in-distribution errors; VRRL broadens this via replay

## Relevance

Directly extends the vault's VLM RL thread (SVR-R1, Video-RTS, Aha Moment Revisited) with a complementary finding: while Aha Moment Revisited shows VLM self-verification fails at inference time, VRRL shows that RL training can be restructured to produce grounded self-reflection via trajectory masking and replay. The experience replay mechanism also connects to ARMOR's off-policy anchor approach — both inject out-of-distribution trajectories to prevent the policy from collapsing to a narrow on-policy distribution.

## My Thoughts

<!-- Add your own notes here -->
