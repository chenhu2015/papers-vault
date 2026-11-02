---
title: "InterQ-RL: Interaction-Aware Correction of Execution Mismatch in Quantized Agentic RL"
authors: ["Yingbo Hao", "Song Liu", "Guanghua Yu", "Zhaojing Zhou", "Jianchen Zhu", "Yi Zou"]
date: 2026-11-02
arxiv_id: "2610.35303v1"
url: "http://arxiv.org/abs/2610.35303v1"
score: 0.79
topics: [agentic RL, RL training, reinforcement learning, LLM agent]
status: unread
---

# InterQ-RL: Interaction-Aware Correction of Execution Mismatch in Quantized Agentic RL

## Summary

InterQ-RL corrects the residual execution mismatch that persists after standard quantization alignment in multi-turn agentic RL: even when current-token rollout-learner ratios are aligned, the state-reaching policy history can be mismatched, distorting credit. It applies bounded execution-prefix correction over this history, allocates correction strength across action segments by effective support under a fixed displacement budget, and requires no additional model forward pass. Evaluated on ALFWorld, WebShop, and ScienceWorld with W8A8-KV8 quantization (4B–30B dense and MoE backbones), InterQ-RL matches BF16 performance within 0.7 points and exceeds it in two settings.

## Key Contributions

- Diagnoses residual rollout-learner mismatch: existing quantization alignment corrects current-token ratios but ignores the cumulative state-reaching policy history, which accumulates mismatch across interaction turns
- Bounded execution-prefix correction over state-reaching history, with credit strength allocated by effective support under a fixed displacement budget
- No additional model forward pass required
- W8A8-KV8 performance matches BF16 within 0.7pp and exceeds it in 2/4 backbone-environment settings across ALFWorld, WebShop, ScienceWorld

## Relevance

InterQ-RL addresses a practical bottleneck in the long-horizon agentic RL thread (multi-turn rollout cost) from the training efficiency angle rather than the credit assignment angle — directly complementing ConCal and SCOPE from today's digest. It provides a path to near-BF16 quality at 8-bit compute, which is critical for the large-scale training that QwenGyre and FOCUS require.

## My Thoughts

<!-- Add your own notes here -->
