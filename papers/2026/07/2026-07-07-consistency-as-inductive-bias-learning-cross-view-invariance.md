---
title: "Consistency as Inductive Bias: Learning Cross-View Invariance for Robust Multimodal Reasoning"
authors: ["Xin Zou", "Haolin Deng", "Yibo Yan", "Shuliang Liu", "Kening Zheng", "Zhiwei Jin", "Chen Chen", "Haonan Lu", "Xuming Hu"]
date: 2026-07-07
arxiv_id: "2606.29812v1"
url: "http://arxiv.org/abs/2606.29812v1"
score: 0.76
topics: [GRPO, multimodal, vision-language, VLM, RL training]
status: unread
---

# Consistency as Inductive Bias: Learning Cross-View Invariance for Robust Multimodal Reasoning

## Summary

ConsistRoll identifies cross-view consistency — the constraint that semantically equivalent visual inputs should yield the same answer — as a missing inductive bias in RLVR training. Standard GRPO assigns pointwise rewards to each visual input independently, so even with data augmentation transformed views are rewarded separately and provide little signal once within-view rewards saturate. ConsistRoll reuses the GRPO group-sampling mechanism to place original and transformed views in the same generation group, issuing a joint reward only when both completions are correct and consistent, without extra generation overhead or annotations.

## Key Contributions

- Identifies cross-view consistency as a structural gap in RLVR/GRPO training objectives
- Joint-reward group sampling: original + semantically invariant transformed view share one GRPO group
- No extra generation cost relative to standard GRPO
- Theoretical analysis: introduces a cross-view correction term that penalizes view-dependent advantage collapse, absent from data augmentation alone

## Relevance

Directly extends the RLVR failure mode thread by identifying a fourth distinct failure mode — view-dependent advantage collapse — complementing the triad established in the vault (SeL information self-locking, TA-GRPO diversity collapse, RL-PLUS capability boundary collapse). ConsistRoll's mechanism is structurally similar to TA-GRPO's question rephrasing (both generate semantically equivalent variants and enforce consistency at the group level) but operates at the visual input level rather than the question-text level, making them orthogonal and combinable.

## My Thoughts

<!-- Add your own notes here -->
