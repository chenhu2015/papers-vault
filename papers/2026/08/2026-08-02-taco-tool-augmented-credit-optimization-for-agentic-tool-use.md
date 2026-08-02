---
title: "TACO: Tool-Augmented Credit Optimization for Agentic Tool Use"
authors: ["Mingkuan Feng", "Jinyang Wu", "Hao Gu", "Fangrui Lv", "Ruihan Jin", "Chuyuan Zhang", "Zhengqi Wen", "Jianhua Tao"]
date: 2026-06-29
arxiv_id: "2606.30251"
url: "https://arxiv.org/abs/2606.30251"
score: 0.87
topics: [agentic RL, tool use, GRPO, multimodal models, reward model]
status: unread
---

# TACO: Tool-Augmented Credit Optimization for Agentic Tool Use

## Summary

TACO introduces a GRPO variant for code-tool multimodal agents with two coupled advantage channels: DAPR (Differential Answer-Probe Reward), which credits each tool call by comparing outcomes with vs. without the call using probe tokens — no external judge needed — and OGAR (Outcome-Gated Advantage Routing), which restricts outcome credit to responsible trajectory segments based on call outcome. The combination yields a self-supervised, judge-free per-tool-call credit mechanism that improves accuracy while learning to invoke tools only when they help.

## Key Contributions

- **DAPR**: Probe tokens inserted into the model's reasoning elicit predictions with and without a tool; the reward difference quantifies the call's value (positive = useful, negative = misleading, zero = neutral) — naturally robust to probe-hacking because it's a difference, not an absolute probe score
- **OGAR**: Parameter-free rule that routes outcome advantage only to responsible segments conditioned on call outcome, suppressing wasted tool calls without an explicit cost term
- **Self-supervised credit with no auxiliary judge**: Reuses the existing answer checker, making TACO applicable without a separate critic or process reward model
- **Two-stage SFT+RL pipeline** demonstrated on visual QA benchmarks across perception, reasoning, and general multimodal tasks

## Relevance

TACO directly advances the tool-use credit assignment problem that has been a persistent thread since TAO-RL and the Gap #16 family — but operates at a fundamentally different granularity: per-tool-call rather than per-token or per-turn. DAPR's probe-based differential is a new self-supervised credit mechanism distinct from all prior entropy-based and statistics-based approaches in the vault, making it orthogonal to STARE/ERPO/GRSD. It also extends the multimodal RL thread (previously thin in the vault) to code-tool agents.

## My Thoughts

<!-- Add your own notes here -->
