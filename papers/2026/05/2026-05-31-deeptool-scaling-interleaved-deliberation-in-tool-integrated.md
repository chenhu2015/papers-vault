---
title: "DeepTool: Scaling Interleaved Deliberation in Tool-Integrated Reasoning via Process-Supervised Reinforcement Learning"
authors: ["Yang He", "Xiao Ding", "Bibo Cai", "Yufei Zhang", "Kai Xiong", "Zhouhao Sun", "Bing Qin", "Ting Liu"]
date: 2026-05-31
arxiv_id: "2605.29568"
url: "https://arxiv.org/abs/2605.29568"
score: 0.88
topics: [agentic RL, tool use, GRPO, reward model, LLM agent]
status: unread
---

# DeepTool: Scaling Interleaved Deliberation in Tool-Integrated Reasoning via Process-Supervised Reinforcement Learning

## Summary

DeepTool scales deliberate thinking within the interleaved think-act-observe loop for tool-integrated reasoning using a GRPO-based Action-Centric Process Reward that supervises intermediate thinking at every tool invocation. Combined with adversarial trajectory synthesis for robustness and self-correction, it boosts Qwen2.5-7B substantially on AIME24 (3.2% to 40.4%) and HMMT25 (0% to 28.6%), confirming that dense step-level process supervision at tool boundaries enables strong planning and self-correction.

## Key Contributions

- Process-Supervised RL based on GRPO with Action-Centric Process Reward: dense step-level supervision at each tool invocation rather than outcome-only reward
- Synthesis pipeline that evolves extended thinking into interleaved trajectories with adversarial perturbations, improving robustness and self-correction
- Demonstrates interleaved thinking is cost-effective: token cost-effectiveness analysis confirms optimal performance-efficiency tradeoff
- Massive benchmark gains: AIME24 3.2% → 40.4%, HMMT25 0% → 28.6% on Qwen2.5-7B

## Relevance

Directly advances the agentic RL + tool use thread, adding a strong process reward signal at each tool call. Complements PRO-CUA (also in today's digest) by tackling the same problem space from the reasoning/deliberation angle rather than the GUI/action diversity angle.

## My Thoughts

<!-- Add your own notes here -->
