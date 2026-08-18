---
title: "Explicit Language Memory for Long-Horizon Planning in Vision-Language-Action Models"
authors: ["Houze Xu", "Jizhong Li", "Ziyi Ye"]
date: 2026-08-18
arxiv_id: "2608.04765"
url: "http://arxiv.org/abs/2608.04765v1"
score: 0.77
topics: [vision-language models, VLM, multimodal, agentic]
status: unread
---

# Explicit Language Memory for Long-Horizon Planning in Vision-Language-Action Models

## Summary

The paper proposes a hierarchical VLA architecture with an explicit language-memory module that converts discrete temporal observations into a coherent textual memory sequence with temporal logic. A high-level VLM performs semantic reasoning via a VQA training paradigm while a low-level VLA executes continuous control; the high-level VLM recursively updates both memory and subtask instructions using the previous memory as a contextual anchor, enabling persistent temporal tracking and dynamic error correction. Experiments in simulation and on a real robot platform show improved success rate and robustness on complex long-horizon tasks while preserving the VLM backbone's semantic representations.

## Key Contributions

- Explicit language-memory module that converts temporal observations into a textual memory sequence with temporal logic, decoupling high-level VLM reasoning from low-level VLA control
- VQA training paradigm for the high-level VLM: preserves VLM backbone's semantic representations without degrading them through end-to-end action fine-tuning
- Recursive memory-and-instruction update: previous memory as contextual anchor enables persistent temporal tracking and mid-trajectory correction
- Sim-to-real experiments on a real robotic platform confirming improved success and interpretability

## Relevance

This paper addresses the VLM angle of the interest profile that the vault has been lighter on compared to the RL training thread. The VQA training paradigm for the high-level VLM is a specific instance of the end-to-end action fine-tuning degradation problem — the concern that fine-tuning on continuous control reduces the backbone VLM's semantic grounding. The hierarchical decoupling (VLM for reasoning, VLA for control) is architecturally related to the SeekJudge role-decomposition (Aug 16): both split a monolithic pipeline into specialized sub-roles trained separately, with a clean interface between them.

## My Thoughts

<!-- Add your own notes here -->
