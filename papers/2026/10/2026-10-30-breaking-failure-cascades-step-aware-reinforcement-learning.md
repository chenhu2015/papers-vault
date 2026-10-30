---
title: "Breaking Failure Cascades: Step-Aware Reinforcement Learning for Medical Multimodal Reasoning"
authors: ["Junha Jung", "Minbyul Jeong", "Suhyeon Lim", "Sungwook Jung", "Jaehoon Yun", "Taeyun Roh", "Mujeen Sung", "Jaewoo Kang"]
date: 2026-10-30
arxiv_id: "2606.31825v2"
url: "http://arxiv.org/abs/2606.31825v2"
score: 0.88
topics: [vision-language, VLM, GRPO, reward model, multimodal]
status: unread
---

# Breaking Failure Cascades: Step-Aware Reinforcement Learning for Medical Multimodal Reasoning

## Summary

MRPO (Medical Reasoning-aware Policy Optimization) is a GRPO variant that addresses sparse credit assignment in multimodal LLM reasoning by assigning exponentially larger penalties to tokens in earlier invalid reasoning steps when the final answer is incorrect. This step-level process reward breaks failure cascades — early reasoning errors that propagate to wrong final answers — reducing their frequency from 58.6% to 13.4% on medical VQA benchmarks. On Qwen3-VL-8B-Thinking, MRPO consistently outperforms standard GRPO and surpasses medical MLLMs 4× its size.

## Key Contributions

- Identifies cascading errors from early-stage reasoning failures as the dominant error mode in medical VQA
- MRPO assigns exponentially larger penalties to earlier invalid reasoning steps, not just the final answer
- Step-level credit assignment without requiring annotated step-level supervision — derived from final answer correctness
- Reduces early-stage reasoning failures from 58.6% to 13.4%; outperforms HuatuoGPT-Vision-34B with 8B model

## Relevance

This is the first clear win for the VLM RL credit assignment thread (17 entries, 2 prior consecutive zeros). MRPO directly addresses the step/token-level credit problem for VLMs but via a different vocabulary — "failure cascade" and "step-aware" rather than "step reward" or "token reward" — explaining why prior ti:-based searches missed it. The exponential penalty weighting by position is a concrete, simple mechanism worth noting for the broader credit assignment cluster.

## My Thoughts

<!-- Add your own notes here -->
