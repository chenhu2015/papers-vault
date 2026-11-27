---
title: "Agentic Reinforcement Learning with Immediate and Prospective Credit Assignment for Medical Visual Reasoning"
authors: ["Yuqi Cheng", "Rui Meng", "Yijin Li", "Chandra Sekhar Reddy Edula", "Xiuwei Zhang"]
date: 2026-11-25
arxiv_id: "2611.33777v1"
url: "https://arxiv.org/abs/2611.33777"
score: 0.85
topics: [agentic RL, GRPO, multimodal models, VLM, tool use]
status: unread
---

# Agentic Reinforcement Learning with Immediate and Prospective Credit Assignment for Medical Visual Reasoning

## Summary

MedPACT introduces two complementary credit signals for GRPO-based agentic RL on medical VQA: an immediate credit that isolates how observed content improves the current answer versus matched alternatives, and a prospective credit estimating how the observation guides subsequent actions. Both credits are assigned to tool-call tokens within standard GRPO alongside trajectory-level outcome supervision, using a single VLM at training time only. Achieves improved accuracy and OOD generalization across six medical VQA benchmarks at 4B and 8B scale with substantially lower inference cost than multi-model alternatives.

## Key Contributions

- Content-controlled immediate credit: compares next-action outcomes under real vs. matched alternative observations, isolating content effect from history
- Prospective credit: estimates how well the current observation improves subsequent decision quality
- Both credit forms integrated into tool-call tokens within GRPO; no additional models at inference
- Demonstrates avoidance of repeated observations and evidence-guided inspection in case studies

## Relevance

The fifth entry in the agentic credit assignment thread (TACA, MSPO, ViCARD, TWICE, now MedPACT). Unlike TACA (tool-token credit in search agents) and MSPO/ViCARD (module/token-level credit in visual reasoning), MedPACT addresses the sequential observation selection problem: which evidence to gather next, not just how to weight what was gathered. The immediate+prospective decomposition is a new framing not seen in prior thread entries.

## My Thoughts

<!-- Add your own notes here -->
