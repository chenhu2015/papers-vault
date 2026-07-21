---
title: "DyCo-RL: Dynamic Cross-Modal Coordination for Visual Reasoning"
authors: ["Hangui Lin", "Yan Shu", "Zhengyang Liang", "Chi Liu", "Xiangrui Liu", "Minghao Qin", "Teng Long", "Zheng Liu", "Nicu Sebe"]
date: 2026-07-21
arxiv_id: "2606.08035"
url: "https://arxiv.org/abs/2606.08035"
score: 0.88
topics: [multimodal models, vision language models, agentic RL, GRPO, VLM, vision-language]
status: unread
---

# DyCo-RL: Dynamic Cross-Modal Coordination for Visual Reasoning

## Summary

DyCo-RL uncovers a cross-modal coordination breakdown in multimodal RLVR: token-level analysis shows VLMs frequently fail to alternate between visual evidence extraction and textual synthesis during CoT reasoning, causing accuracy failures causally linked to the coordination gap. The framework uses Fisher-Rao geodesic distance to classify tokens as visually- or text-oriented, evaluates the alignment between each token's actual attention and its assigned role, and reweights policy gradient advantages accordingly. Algorithm-agnostic design applies to any RLVR backbone (GRPO, DAPO), yielding consistent gains across seven benchmarks on Qwen2.5-VL-3B/7B.

## Key Contributions

- Token-level causal analysis establishing cross-modal coordination breakdown as a distinct failure mode in multimodal RLVR (separate from thinking-answer inconsistency in CORA and visual sensitivity in SIVA-RL)
- Fisher-Rao geodesic distance as a principled measure of within-modality attention shifts, assigning each token to visually-oriented or text-oriented functional roles
- Alignment-guided advantage reweighting: advantage scores scaled by the match between a token's actual attention allocation and its assigned modal role
- Algorithm-agnostic implementation: compatible with GRPO and DAPO, applied to Qwen2.5-VL-3B/7B across seven benchmarks

## Relevance

DyCo-RL introduces a new axis of VLM RL optimization that is orthogonal to the failure modes already in the vault: CORA addressed thinking-answer semantic inconsistency at the trace level, SIVA-RL addressed visual sensitivity at the sample level, and FWS addressed language prior exploitation before RL via SFT warm-start. DyCo-RL addresses the token-level cross-modal attention allocation during RLVR optimization itself — making it the most fine-grained of the four VLM faithfulness approaches and directly extending the token-level credit assignment thread (EGRSD, TACO, RL-ZVP) into the multimodal setting via attention-role alignment rather than entropy or probability signals.

## My Thoughts

<!-- Add your own notes here -->
