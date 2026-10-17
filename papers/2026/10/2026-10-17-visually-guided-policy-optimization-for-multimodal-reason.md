---
title: "Visually-Guided Policy Optimization for Multimodal Reasoning"
authors: ["Zengbin Wang", "Feng Xiong", "Liang Lin", "Xuecai Hu", "Yong Wang", "Yanlin Wang", "Man Zhang", "Xiangxiang Chu"]
date: 2026-04-10
arxiv_id: "2604.09349v2"
url: "http://arxiv.org/abs/2604.09349v2"
score: 0.88
topics: [VLM RL credit assignment, vision language models, RLVR, reinforcement learning, agentic RL]
status: unread
---

# Visually-Guided Policy Optimization for Multimodal Reasoning

## Summary

VGPO addresses temporal visual forgetting in RLVR by introducing a Visual Attention Compensation (VAC) mechanism that amplifies visually salient cues and progressively raises visual expectations over reasoning steps. A dual-grained advantage re-weighting strategy highlights tokens with high visual activation (intra-trajectory) while prioritising trajectories that accumulate strong visual attention (inter-trajectory). The credit signal is derived entirely from the model's own attention distributions rather than outcome labels, extending the VLM RL credit assignment thread with an attention-grounded approach.

## Key Contributions

- Visual Attention Compensation (VAC): leverages visual similarity to localise and amplify visual cues; escalates visual expectations in later reasoning steps to counteract forgetting
- Dual-grained advantage re-weighting: intra-trajectory highlights tokens with relatively high visual activation; inter-trajectory prioritises rollouts with superior cumulative visual attention
- Diagnosis: empirical analysis confirms temporal visual forgetting as a distinct failure mode — attention to visual tokens decays predictably as reasoning chain lengthens
- Strong results on math multimodal reasoning and visual-dependent tasks without domain-specific inductive biases

## Relevance

The dual-grained attention-weighted advantage is a fourth mechanism for token-level credit in VLM RL, joining value-difference (LVRL), likelihood-differential (OWLET), and claim-decomposition (SPLIT-RL). The temporal forgetting framing reframes the credit problem as a dynamic attention drift problem rather than a static token-importance problem.

## My Thoughts

<!-- Add your own notes here -->
