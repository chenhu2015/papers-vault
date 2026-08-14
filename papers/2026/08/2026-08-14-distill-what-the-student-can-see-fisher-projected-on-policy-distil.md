---
title: "Distill What the Student Can See: Fisher-Projected On-Policy Distillation for Vision-Language Models"
authors: ["Leyan Xue", "Feng Xiong", "Mingjun Ma", "Changqing Zhang"]
date: 2026-08-02
arxiv_id: "2608.01263v2"
url: "http://arxiv.org/abs/2608.01263v2"
score: 0.75
topics: [vision language models, multimodal models, VLM]
status: unread
---

# Distill What the Student Can See: Fisher-Projected On-Policy Distillation for Vision-Language Models

## Summary

FP-OPD addresses capacity mismatch in standard OPD: teacher corrections can depend on visual distinctions a compact student cannot represent, and forcing the full teacher distribution worsens performance. It estimates the student's local visual tangent space via continuous perturbations and projects the teacher–student log-probability gap onto this space under the student's Fisher metric, yielding a capacity-aware target that distills only what the student can learn. In 8B-to-2B VLM distillation, FP-OPD improves all seven evaluated benchmarks, gaining 1.60 points over standard OPD on average.

## Key Contributions

- Identifies and empirically validates **OPD capacity mismatch**: as the distillation target approaches the complete teacher distribution, the student realizes less of the prescribed shift and achieves worse downstream performance
- **Visual tangent space estimation**: uses continuous visual perturbations to estimate the student's locally realizable subspace
- **Fisher-metric projection**: projects the centered teacher–student log-probability gap onto the visual tangent space under the student's Fisher metric, yielding a capacity-aware target
- 8B-to-2B VLM distillation: +2.77 points over pretrained student, +1.60 points over standard OPD across 7 multimodal benchmarks

## Relevance

FP-OPD introduces a new dimension to the vault's OPD mechanism taxonomy: capacity-aware projection. Where previous OPD variants (RP-OPSD, DASH, SSOPD, SOD) focused on *which tokens* receive supervision or *when* supervision is applied, FP-OPD focuses on *which direction* of the teacher correction is realizable by the student — a fundamentally different axis. This is particularly important for the multimodal OPD thread (VAD, CFPO): teacher visual corrections that exceed the student's representational capacity are not just unhelpful, they actively harm performance.

## My Thoughts

<!-- Add your own notes here -->
