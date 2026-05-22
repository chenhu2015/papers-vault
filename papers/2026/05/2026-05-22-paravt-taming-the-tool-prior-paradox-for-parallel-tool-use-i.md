---
title: "ParaVT: Taming the Tool Prior Paradox for Parallel Tool Use in Agentic Video Reinforcement Learning"
authors: ["Zuhao Yang", "Kaichen Zhang", "Sudong Wang", "Keming Wu", "Zhongyu Yang", "Bo Li", "Xiaojuan Qi", "Shijian Lu", "Xingxuan Li", "Lidong Bing"]
date: 2026-05-22
arxiv_id: "2605.20342"
url: "https://arxiv.org/abs/2605.20342"
score: 0.85
topics: [agentic RL, VLM, tool use, GRPO, multimodal models]
status: unread
---

# ParaVT: Taming the Tool Prior Paradox for Parallel Tool Use in Agentic Video Reinforcement Learning

## Summary

ParaVT introduces the first multi-agent end-to-end RL framework for parallel video tool calling in LMMs, dispatching multiple time-window crops in a single turn to enable cleaner context and better fault tolerance than sequential tool calls. The work identifies the 'Tool Prior Paradox': pretrained tool priors simultaneously enable tool exploration but destabilize cold-started structural format and expose skip-tool reward shortcuts under temperature sampling. PARA-GRPO addresses this with targeted format rewards at structural-token positions and per-prompt frame-budget randomization, improving over Qwen3-VL baseline by +7.9% across six long-video benchmarks with training-time format compliance lifted from 0.13 to 0.64.

## Key Contributions

- Parallel video tool calling: first RL-trained LMM framework dispatching multiple crops in a single turn, eliminating sequential error propagation and linear inference scaling
- Tool Prior Paradox diagnosis: pretrained priors are both necessary for tool exploration and responsible for structural format collapse — validated by cross-model ablation
- PARA-GRPO: targeted format reward at collapse-prone structural-token positions + per-prompt frame-budget randomization to prevent skip-tool shortcut
- Empirical generalization finding: RL must cooperate with pretrained tool priors, not override them

## Relevance

Directly extends the video VLM + agentic tool use RL thread (VITAL May 20, ESearch-R1 May 20, CharTool May 18). The Tool Prior Paradox insight is a general finding applicable to any RL fine-tuning of models with pretrained capabilities — the tension between cold-start format stability and exploring existing priors is a recurring challenge in agentic RL.

## My Thoughts

<!-- Add your own notes here -->
