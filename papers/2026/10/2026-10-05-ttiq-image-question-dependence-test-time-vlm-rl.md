---
title: "Harnessing Image Question Dependence for Better VLM Test-time Reinforcement Learning"
authors: ["Xinrui He", "Ting-Wei Li", "Junting Wang", "Mengting Ai", "Xinyu He", "Hanghang Tong", "Jingrui He"]
date: 2026-10-05
arxiv_id: "2609.13296v1"
url: "https://arxiv.org/abs/2609.13296"
score: 0.89
topics: [multimodal models, vision language models, VLM, agentic RL, GRPO, reward model]
status: unread
---

# Harnessing Image Question Dependence for Better VLM Test-time Reinforcement Learning (TTIQ)

## Summary

TTIQ is a test-time RL framework for VLMs that estimates token-level image-question dependence by teacher-forcing sampled responses under the original input and image- or question-ablated variants, then using the resulting likelihood changes to construct a reward that favors jointly grounded responses. The token-level signal also assigns greater positive policy credit to tokens supported by both image and question, directly addressing grounding errors that consensus-based rewards preserve. TTIQ achieves the best average performance at every model scale across eight VQA datasets and generalizes across VLM families without per-dataset training.

## Key Contributions

- Diagnoses two failures of consensus-based test-time RL: gains come from answer normalization rather than content correction, and grounding errors are preserved rather than fixed
- Token-level image-question dependence estimated via likelihood changes under image-ablated and question-ablated teacher-forcing
- Response-level reward that favors jointly grounded, sufficiently confident responses over merely popular ones
- Token-level credit assignment: greater positive policy gradient credit to tokens supported by both image and question
- Best average performance at every model scale on eight VQA datasets; generalizes across VLM families

## Relevance

TTIQ is the second entry in the test-time VLM RL thread (after TTRSD) and adds a 4th VLM credit axis: joint image-question grounding dependence, complementing TPAE's importance axis, persistence-aware credit's verifiability axis, and TTRSD's visual sensitivity axis. Like TTRSD, TTIQ works from model-internal signals without gold labels. Unlike TTRSD (multi-view self-distillation), TTIQ uses counterfactual ablations of inputs rather than rollout diversity — a cleaner separation between the image and question contributions to each token.

## My Thoughts

<!-- Add your own notes here -->
