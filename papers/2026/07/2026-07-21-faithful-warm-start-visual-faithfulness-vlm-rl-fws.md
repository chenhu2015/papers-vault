---
title: "Be Faithful When Response: Returning Fluent and Grounded Answers for Vision-Language Models Reinforcement Learning"
authors: ["Peng", "Lee", "Yin Zhang", "Yanglin Zhang", "Haonan Wu", "Zishan Liu", "Ruoxi Zang", "Xin Zhu", "Jiayin Zheng", "Jian Yao", "Zefeng Ji", "Fei Ma"]
date: 2026-07-21
arxiv_id: "2606.29984"
url: "https://arxiv.org/abs/2606.29984"
score: 0.78
topics: [multimodal models, vision language models, RL training, VLM, RLAIF, vision-language]
status: unread
---

# Be Faithful When Response: Returning Fluent and Grounded Answers for Vision-Language Models Reinforcement Learning

## Summary

This paper identifies language prior exploitation as a failure mode where VLMs generate fluent but visually ungrounded reasoning traces under sparse answer-level RL rewards, because the model defaults to linguistic patterns while neglecting visual evidence. FWS (Faithful Warm-Start) curates FaithfulQA — samples selected from six VQA benchmarks with explicit vision-language causal relationships, then verified by a VLM judge for causal consistency and visual faithfulness — and uses it for SFT before standard RL fine-tuning. The warm-start stage grounds the initial policy in visually faithful reasoning patterns, improving answer accuracy, stabilizing RL training, and reducing visually unsupported reasoning.

## Key Contributions

- Characterization of the language prior exploitation failure mode in VLM RL: fluent but visually ungrounded reasoning traces emerge because language patterns are easier to optimize than visual evidence extraction under sparse outcome rewards
- FaithfulQA: curated dataset from six general VQA benchmarks with explicit vision-language causal relationships across five categories (visual observations, question requirements, commonsense knowledge, domain knowledge, final answer)
- VLM-based judge to ensure causal consistency and visual faithfulness of the curated samples
- Two-stage pipeline: FWS SFT warm-start for visual faithfulness grounding → standard RL with sparse answer-level rewards

## Relevance

FWS addresses a gap not covered by CORA, SIVA-RL, or DyCo-RL: those papers add new supervision signals during RL optimization, while FWS improves the initialization point before RL begins. The language prior exploitation failure mode is distinct from CORA's thinking-answer inconsistency (the trace is coherent but decoupled from the answer), SIVA-RL's visual sensitivity gap (the model doesn't respond to visual perturbations), and DyCo-RL's cross-modal coordination breakdown (attention fails to alternate between modalities) — here the trace is simply language-fluent while ignoring the image entirely. Together these four papers (CORA, SIVA-RL, DyCo-RL, FWS) characterize four orthogonal failure modes in VLM RL visual faithfulness.

## My Thoughts

<!-- Add your own notes here -->
