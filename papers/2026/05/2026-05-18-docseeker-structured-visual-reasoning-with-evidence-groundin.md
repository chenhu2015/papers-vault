---
title: "DocSeeker: Structured Visual Reasoning with Evidence Grounding for Long Document Understanding"
authors: ["Hao Yan", "Yuliang Liu", "Xingchen Liu", "Yuyi Zhang", "Minghui Liao", "Jihao Wu", "Wei Chen", "Xiang Bai"]
date: 2026-04-14
arxiv_id: "2604.12812v5"
url: "http://arxiv.org/abs/2604.12812v5"
score: 0.82
topics: [VLM, GRPO, multimodal, RL training, vision-language]
status: unread
---

# DocSeeker: Structured Visual Reasoning with Evidence Grounding for Long Document Understanding

## Summary

DocSeeker introduces an Analysis-Localization-Reasoning workflow for long visual document understanding, trained in two stages: SFT on expert-distilled structured reasoning traces, then Evidence-aware GRPO jointly optimizing evidence localization and answer accuracy. Evidence-Guided Resolution Allocation addresses memory constraints on multi-page training; the model robustly generalizes from short-page training to ultra-long documents and is synergistic with visual retrieval-augmented generation systems.

## Key Contributions

- Analysis-Localization-Reasoning structured workflow: forces the model to surface where the evidence is before answering
- Evidence-aware GRPO: joint reward signal for both evidence localization accuracy and final answer correctness
- Evidence-Guided Resolution Allocation: adaptive resolution strategy to manage GPU memory on long multi-page documents
- Short-to-long generalization: trained on short documents, generalizes to ultra-long; complements visual RAG pipelines

## Relevance

Evidence-aware GRPO directly advances the process reward / verifiable reward thread (PDCR May 14, verifiable process rewards May 12) applied to VLM long-document understanding. The joint localization+answer GRPO reward is a concrete instantiation of multi-objective reward design that bridges the VLM and RL training interest threads.

## My Thoughts

<!-- Add your own notes here -->
