---
title: "Escape the Language Prior: Mitigating Late-Stage Modality Collapse in Audio Reasoning via Modality-Aware Policy Optimization"
authors: ["Cihan Xiao", "Yiwen Shao", "Chenxing Li", "Xiang He", "Zhenwen Liang", "Steve Yves", "Sanjeev Khudanpur", "Liefeng Bo"]
date: 2026-05-26
arxiv_id: "2605.27741v2"
url: "http://arxiv.org/abs/2605.27741v2"
score: 0.82
topics: [multimodal models, vision language models, GRPO, reinforcement learning, VLM RL credit assignment]
status: unread
---

# Escape the Language Prior: Mitigating Late-Stage Modality Collapse in Audio Reasoning via Modality-Aware Policy Optimization

## Summary

MAPO addresses late-stage modality collapse in audio/omni-modal LLMs during extended chain-of-thought generation, where models abandon the audio signal in favour of language priors. A modality relevance mask is constructed from cross-modal differential entropy between an audio-ablated reference and the multimodal policy, and the policy gradient is concentrated on those tokens; an auxiliary attention loss imposes a temporally scaled penalty on inattention to the source modality. The mechanism is structurally analogous to VGPO's visual attention grounding, showing that modality-aware weighted credit generalises across sensory modalities.

## Key Contributions

- Identifies late-stage modality collapse as a late-chain phenomenon — models start grounded but drift away as CoT length grows
- Modality relevance mask via cross-modal differential entropy: contrast between audio-ablated and full policy identifies which tokens depend on the non-text source
- Auxiliary attention loss branch: temporally scaled penalty encourages sustained attention to source modality throughout reasoning
- Demonstrated on audio benchmarks; relies on native statistical signals — no domain-specific inductive biases

## Relevance

MAPO is a cross-modal counterpart to VGPO: both use attention-based token weighting to counter modality forgetting, but MAPO operates on audio and constructs its mask from an ablated reference rather than intra-model attention scores. Together they establish that temporal modality forgetting during extended CoT generation is a general multimodal RL failure mode — not specific to vision.

## My Thoughts

<!-- Add your own notes here -->
