---
title: "Agent Explorative Policy Optimization for Multimodal Agentic Reasoning"
authors: ["Minki Kang", "Shizhe Diao", "Ryo Hachiuma", "Sung Ju Hwang", "Pavlo Molchanov", "Yu-Chiang Frank Wang", "Byung-Kwan Lee"]
date: 2026-08-03
arxiv_id: "2605.28774"
url: "http://arxiv.org/abs/2605.28774v1"
score: 0.87
topics: [GRPO, agentic RL, multimodal models, VLM, tool use]
status: unread
---

# Agent Explorative Policy Optimization for Multimodal Agentic Reasoning

## Summary

AXPO identifies the "Thinking-Acting Gap" in GRPO-trained multimodal agents: tool use is attempted in only ~30% of rollouts and all-wrong tool-using subgroups arise in ~40% of questions, zeroing the learning signal at exactly the tool calls that need it. The fix resamples each all-wrong tool-using subgroup by fixing the thinking prefix and resampling only the tool call and continuation, paired with uncertainty-based prefix selection for which prefix to fix. SFT+AXPO outperforms SFT+GRPO across nine multimodal benchmarks at three Qwen3-VL-Thinking scales, and an 8B model with AXPO surpasses a 32B baseline on Pass@4 with four times fewer parameters.

## Key Contributions

- Diagnoses two structural GRPO failure modes in multimodal tool use: low tool-attempt rate (~30%) and high all-wrong tool-using subgroup rate (~40%)
- Proposes targeted resampling: fix thinking prefix, resample only the tool call and continuation for all-wrong tool-using subgroups
- Uncertainty-based prefix selection identifies which thinking prefixes are reliable anchors for resampling
- 8B SFT+AXPO beats 32B base model on Pass@4 across nine multimodal benchmarks

## Relevance

AXPO directly extends the Gap #16 (all-fail group) literature to the multimodal tool-use setting, diagnosing two interacting failure modes (low attempt rate + all-wrong subgroup rate) that do not arise in single-modality math reasoning. Its prefix-fixing resampling is structurally different from all nine prior Gap #16 approaches: it does not modify the reward, filter the group, inject proxy rewards, or use contrastive reflection—it restructures *which* completion tokens are resampled. AXPO's "Thinking-Acting Gap" framing complements TACO's DAPR (Aug 2, per-tool-call credit) as the two papers that most directly address the tool-use credit assignment problem in multimodal GRPO.

## My Thoughts

<!-- Add your own notes here -->
