---
title: "IAPO: Input Attribution-Aware Policy Optimization for Tool Use in Small Multimodal Agents"
authors: ["Yifan Yang", "Zhen Zhang", "Jiayi Tian", "Liyan Tan", "Zheng Zhang"]
date: 2026-08-03
arxiv_id: "2606.11652"
url: "http://arxiv.org/abs/2606.11652v1"
score: 0.78
topics: [multimodal models, VLM, vision-language, tool use, agentic RL, reinforcement learning]
status: unread
---

# IAPO: Input Attribution-Aware Policy Optimization for Tool Use in Small Multimodal Agents

## Summary

IAPO addresses RL for multimodal tool use in small language models where binary exact-match rewards fail because multiple valid tool paths exist and ground-truth trajectories are unavailable. Instead of outcome rewards, IAPO aligns the model's input attribution pattern across visual and textual components with that of a stronger teacher model, rewarding tool calls that attend to the same evidence as the expert. On Qwen2.5-VL-3B, IAPO improves VQA accuracy by an average of 3% across six test sets over prior visual tool-use baselines.

## Key Contributions

- Identifies two fundamental limitations of binary rewards for multimodal tool use: multiple valid paths and unavailable ground-truth trajectories
- Attribution alignment reward: measures how well the student's attention over input components matches a stronger teacher's during tool calls
- Applicable to SLMs (3B scale) where binary outcome RL is especially unstable
- 3% average VQA accuracy gain across six benchmarks on Qwen2.5-VL-3B

## Relevance

IAPO connects to two active threads: TACO's per-tool-call credit (Aug 2) and AXPO's Thinking-Acting Gap (today). TACO uses differential outcome probing to assign credit to tool calls; AXPO resamples all-wrong tool-using subgroups. IAPO takes a third path: using teacher attribution as the process reward signal, making the credit signal based on *what the model attends to* rather than *what outcome it achieves*. This is the first paper in the vault to use attention attribution as a direct RL training reward, and it is complementary to PRPO's RVD (visual faithfulness as VLM RL signal, Gap #7) — both reward visual attention patterns, but PRPO targets spatial faithfulness in generation while IAPO targets diagnostic attention in tool-use decisions.

## My Thoughts

<!-- Add your own notes here -->
