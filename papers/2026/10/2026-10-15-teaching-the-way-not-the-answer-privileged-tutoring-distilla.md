---
title: "Teaching the Way, Not the Answer: Privileged Tutoring Distillation for Multimodal Policy Optimization"
authors: ["Shizhe Xiang", "Ke An", "Wenlong Yu", "Yue Liu", "Jian Luan", "Pei Fu", "Qilong Wang"]
date: 2026-10-15
arxiv_id: "2606.07000v1"
url: "https://arxiv.org/abs/2606.07000"
score: 0.78
topics: [VLM, vision-language, RLHF, RLAIF, reward model, multimodal]
status: unread
---

# Teaching the Way, Not the Answer: Privileged Tutoring Distillation for Multimodal Policy Optimization

## Summary

PTD-PO provides dense token-level guidance for RLVR failed rollouts without exposing answers: it constructs privileged hints from spatial attention and intermediate reasoning steps, uses them in-context to produce step-wise token-distribution supervision, and aligns the student's failed rollouts to the hint-augmented reference model. A Top-K Jensen-Shannon divergence objective stabilises distillation under the guided/unguided context distribution shift. Experiments on 2B–8B LVLMs consistently outperform RLVR and distillation baselines while reducing entropy collapse.

## Key Contributions

- Privileged hint construction: spatial attention guidance + intermediate reasoning steps without answer leakage
- In-context hint injection produces step-wise token-distribution supervision for failed rollouts
- Top-K Jensen-Shannon divergence objective: focuses alignment on informative token probabilities, reduces memory overhead
- Addresses entropy collapse, a failure mode of RLVR that TRM (Oct 14) also flagged via score polarisation
- Works within the student's own answer-free context at inference — no overhead

## Relevance

Complements OWLET and SPLIT-RL within the VLM RL credit thread by attacking the failed-rollout supervision gap (the symmetric problem to what LVRL attacks via value estimation). PTD-PO's spatial attention hint is a spatially grounded form of supervision analogous to OWLET's question-conditioned local window, but applied to static images rather than video and via in-context hinting rather than likelihood redistribution.

## My Thoughts

<!-- Add your own notes here -->
