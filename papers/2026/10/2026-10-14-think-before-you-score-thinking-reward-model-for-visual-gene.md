---
title: "Think Before You Score: Thinking Reward Model for Visual Generation"
authors: ["Xuehai Bai", "Zhenchen Tang", "Yang Shi", "Dianyi Wang", "Tengfei Liu", "Wanshun Su", "Xuanyu Zhu", "Ruohui Wang", "Haiwen Diao", "Haotian Wang", "Xiaoling Gu", "Yuanxing Zhang"]
date: 2026-10-14
arxiv_id: "2609.37372v1"
url: "http://arxiv.org/abs/2609.37372v1"
score: 0.80
topics: [reward model, GRPO, multimodal models, vision-language, RL training]
status: unread
---

# Think Before You Score: Thinking Reward Model for Visual Generation

## Summary

Proposes TRM (Thinking Reward Model), which formulates case-adaptive rubrics before scoring visual generation outputs rather than mapping directly to scalars, yielding fine-grained pointwise rewards for image generation/editing. Identifies score polarization as a failure mode of conventional pairwise preference optimization and introduces PD-GRPO (Pairwise Dual-Group GRPO) to leverage pairwise supervision while preserving fine-grained scoring. TRM achieves state-of-the-art among open-source reward models and its rewards improve diverse visual generation models when used as RL signals.

## Key Contributions

- Case-adaptive rubric formulation before scoring (TRM): determines what matters per instance before judging quality
- PD-GRPO (Pairwise Dual-Group GRPO): new GRPO variant that uses pairwise supervision to improve reward discrimination while preserving pointwise fine-grained scoring; addresses score polarization
- State-of-the-art among open-source visual reward models on image generation/editing benchmarks
- Demonstrates TRM rewards translate to effective RL optimization signals for visual generation models

## Relevance

Introduces PD-GRPO as a new GRPO variant, extending the GRPO+reward-model thread into the visual generation domain. The case-adaptive rubric framing connects to the "think before you act" paradigm seen in step-credit approaches; the score-polarization diagnosis is a novel failure mode for the reward-model-as-RL-signal pipeline relevant to the step-credit cluster.

## My Thoughts

<!-- Add your own notes here -->
