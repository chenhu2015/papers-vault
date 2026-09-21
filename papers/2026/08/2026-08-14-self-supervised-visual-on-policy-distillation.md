---
title: "Self-Supervised Visual On-Policy Distillation"
authors: ["Yijiang Li", "Yijun Liang", "Yunjie Tian", "Bingyang Wang", "Ke Zhang", "Zhenfei Yin", "Di Fu", "Philip Torr", "Nuno Vasconcelos"]
date: 2026-08-14
arxiv_id: "2608.14144v1"
url: "http://arxiv.org/abs/2608.14144v1"
score: 0.84
topics: [multimodal models, vision language models, VLM, multimodal, vision-language]
status: unread
---

# Self-Supervised Visual On-Policy Distillation

## Summary

S²VOPD eliminates the need for ground-truth annotations, scalar rewards, or a stronger teacher in visual on-policy distillation by constructing learning signals from asymmetric augmented views: the student sees a strongly augmented image while the teacher sees the original, creating a free teacher-student asymmetry without privileged supervision. Systematic ablations find that asymmetry direction matters (symmetric self-distillation hurts), augmentation strength follows an inverted-U curve, and augmentations must preserve question-relevant evidence. Applied to Qwen3.5-4B, this raises aggregate accuracy on six fine-grained visual perception benchmarks from 70.7% to 77.4%.

## Key Contributions

- Inverts the standard privileged-teacher framing: information asymmetry is created by subtracting from the student (strong augmentation) rather than adding to the teacher
- No ground-truth labels, rewards, or stronger teacher required — on-policy signals are entirely self-generated from augmented views
- Three design principles validated empirically: asymmetry is necessary, moderate strength is optimal, augmentations must preserve task-relevant visual content
- Broad benchmark gains (70.7% → 77.4% on Qwen3.5-4B) above all open-source models compared across six fine-grained visual perception tasks

## Relevance

Directly fills the long-running SFT-free VLM RL gap tracked since Sep 14. Unlike prior VLM RL papers that require scalar rewards or ground-truth answers (V-Zero, ACRE), S²VOPD is fully annotation-free, operating via asymmetric augmentation. The connection to the on-policy distillation cluster (STRIDE/RetireOPD/APEx) is structural: it uses the same on-policy teacher-student update loop but constructs the teacher asymmetry from augmentation rather than model size or answer labels.

## My Thoughts

<!-- Add your own notes here -->
