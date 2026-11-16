---
title: "Overcoming Scaling Limits in On-Policy Self-Distillation for LLM Reasoning"
authors: ["Md. Ismail Hossain", "Humaira Kousar", "Isidora Chara Tourni"]
date: 2026-09-29
arxiv_id: "2609.37915v1"
url: "https://arxiv.org/abs/2609.37915"
score: 0.85
topics: [RL training, RLAIF, GRPO, reward model, reinforcement learning]
status: unread
---

# Overcoming Scaling Limits in On-Policy Self-Distillation for LLM Reasoning

## Summary

OASIS separates scaffold correctness from context correctness in OPSD via factorial analysis, finding scaffold correctness has stronger downstream impact. Standard OPSD's imitation gap — caused by supervising mostly unverified trajectories — shrinks with scale but persists, explaining OPSD's 0.14-point gain at 8B vs. 3.05-point gain at 1.7B. OASIS fixes this by supervising on verified on-policy scaffolds while using unverified model attempts (not gold solutions) as teacher context, improving over base models by 3.2–3.8 points on AIME 2024/2025 and HMMT 2025.

## Key Contributions

- Factorial analysis separating scaffold correctness vs. context correctness in OPSD — scaffold correctness dominates
- Diagnoses "imitation gap": standard OPSD supervises mostly unverified trajectories, introducing information the student can't access at inference
- OASIS: verified-by-label on-policy scaffolds + unverified model attempts as teacher context (no gold solutions needed)
- Preserves OPSD's effectiveness as models scale: 3.05→0.14 points for OPSD vs. 3.2–3.8 points consistently for OASIS

## Relevance

Pairs directly with "Diagnosing OPSD" (also Nov 16) to explain the OPSD failure taxonomy: Diagnosing OPSD identifies the failure modes; OASIS identifies the specific structural fix (verified scaffolds) that preserves effectiveness at scale. Together they define the boundary between working and broken OPSD configurations. The "imitation gap" mechanism also connects to GIFT (gradient geometry detecting when teacher information is inaccessible to student) and to Reframe (observation-aligned MOPD, ensuring teacher sees same observations as student).

## My Thoughts

<!-- Add your own notes here -->
