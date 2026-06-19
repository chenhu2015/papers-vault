---
title: "RUBAS: Rubric-Based Reinforcement Learning for Agent Safety"
authors: ["Xian Qi Loye", "Qinglin Su", "Zhexin Zhang", "Shiyao Cui", "Qi Zhu", "Fei Mi", "Hongning Wang", "Minlie Huang"]
date: 2026-06-19
arxiv_id: "2606.04051v1"
url: "http://arxiv.org/abs/2606.04051v1"
score: 0.79
topics: [tool use, agentic RL, reward model, LLM agent, RLHF]
status: unread
---

# RUBAS: Rubric-Based Reinforcement Learning for Agent Safety

## Summary

Tool-enabled LLM agents face safety challenges tied to real-world execution; coarse refusal signals and static supervision struggle to balance safety with useful tool execution across diverse agentic risks. RUBAS decomposes agent behavior into four rubric dimensions — tool-use safety, argument safety, response safety, and helpfulness — to provide fine-grained interpretable rewards over complete agent trajectories, enabling RL to optimize safe tool use while preserving task completion. Experiments across multiple agent safety benchmarks show RUBAS improves safety over standard alignment baselines and reduces tool-grounded hallucinations.

## Key Contributions

- Identifies four agentic safety dimensions: tool-use safety (which tools are called), argument safety (what arguments are passed), response safety (what is returned to the user), helpfulness (task completion)
- Rubric-based multi-dimensional reward over complete trajectories rather than binary refusal/completion signals
- RL training with RUBAS improves safety and reduces tool-grounded hallucinations while maintaining competitive utility
- Addresses the safety-utility tradeoff that coarse alignment methods fail on by providing directional fine-grained reward

## Relevance

Applies the rubric-based reward design (DEEPRUBRIC Jun 18, ARES today, ARBOR today) specifically to the *safety* dimension of agentic tool use — an area that HARVE (Jun 8) and PRIME (Jun 17) addressed from the reward-hacking angle. RUBAS is complementary: HARVE/PRIME prevent the model from hacking the reward signal, RUBAS ensures the reward signal itself captures the full safety-utility tradeoff via structured rubric decomposition rather than a single scalar. The four-dimension decomposition (tool-use, argument, response, helpfulness) is a clean operationalization of the multi-dimensional alignment problem.

## My Thoughts

<!-- Add your own notes here -->
