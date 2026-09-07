---
title: "EvoHarness-RL: Learning Self-Evolving Runtime Harness for Long-Horizon LLM Agents"
authors: ["Xuying Ning", "Dongqi Fu", "Tianxin Wei", "Hanqing Zeng", "Yuanchen Bei", "Bingxuan Li", "Zihao Li", "Qifan Wang", "Xiang Shen", "Yifan Wu", "Jiayi Liu", "Hong Li", "Yinglong Xia", "Xiangjun Fan", "Hanghang Tong", "Jingrui He"]
date: 2026-09-07
arxiv_id: "2608.05446v1"
url: "https://arxiv.org/abs/2608.05446"
score: 0.81
topics: [agentic RL, LLM agent, tool use, GRPO, reinforcement learning, RL training]
status: unread
---

# EvoHarness-RL: Learning Self-Evolving Runtime Harness for Long-Horizon LLM Agents

## Summary

EvoHarness-RL treats the agent's external workspace (harness) as a learnable policy over Belief, Progress, and Experience (BPE) state rather than a static scaffold. Supervised harness fine-tuning teaches the agent the harness action space; cost-aware GRPO then explores when to read, update, and consolidate that state. Two emergent dynamics are observed: harness annealing (training internalizes recurring harness-use patterns into the model, reducing explicit tool calls) and harness evolution (progress updates and experience consolidation refine the harness into a compact task-adaptive substrate). On ALFWorld with Qwen3-8B, the system reaches 96.9% success.

## Key Contributions

- BPE (Belief, Progress, Experience) external harness state exposed as a policy-facing action space — harness use is trained, not hand-engineered
- Supervised harness fine-tuning (SFT stage) + cost-aware GRPO (RL stage) — cost-awareness penalizes unnecessary external state access
- Harness annealing: recurring harness-use patterns are internalized into the model weights over training, shifting from frequent calls to selective access
- Harness evolution: experience consolidation progressively compresses the external substrate toward task-relevant content

## Relevance

EvoHarness-RL extends the agentic RL efficiency thread (SINKFLEX-RL's attention-kernel co-design, SCALECUA's curriculum-aware rollout allocation, HARTS's rollout tree prefix sharing) by adding a fifth axis: external workspace policy learning. The harness-annealing phenomenon directly connects to the base model prior finding from Demystifying RL Post-Training — tool-use patterns that are internalized (annealed) into model weights are functionally equivalent to the model acquiring those behaviors via base model prior rather than explicit tool calls, providing a trainable pathway toward the SFT-free VLM RL gap.

## My Thoughts

<!-- Add your own notes here -->
