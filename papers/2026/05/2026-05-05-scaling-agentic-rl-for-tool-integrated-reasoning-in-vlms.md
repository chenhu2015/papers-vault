---
title: "Scaling Agentic Reinforcement Learning for Tool-Integrated Reasoning in VLMs"
authors: ["Meng Lu", "Ran Xu", "Yi Fang", "Wenxuan Zhang", "Yue Yu", "Gaurav Srivastava", "Yuchen Zhuang", "Mohamed Elhoseiny", "Charles Fleming", "Carl Yang", "Zhengzhong Tu", "Yang Xie", "Guanghua Xiao", "Hanrui Wang", "Di Jin", "Wenqi Shi", "Xuan Wang"]
date: 2025-11-24
arxiv_id: "2511.19773v1"
url: "http://arxiv.org/abs/2511.19773v1"
score: 0.84
topics: [agentic RL, tool use, vision language models, VLM, LLM agent]
status: unread
---

# Scaling Agentic Reinforcement Learning for Tool-Integrated Reasoning in VLMs

## Summary

VISTA-Gym is a scalable training environment unifying 7 multimodal reasoning tasks across 13 datasets with a standardized interface for visual tools (grounding, parsing), executable interaction loops, and verifiable feedback signals—enabling visual agentic RL at scale for VLMs. VISTA-R1 is trained end-to-end via multi-turn trajectory sampling and RL, learning to interleave tool invocation with agentic reasoning. VISTA-R1-8B outperforms state-of-the-art similarly-sized baselines by 9.51%–18.72% across 11 reasoning-intensive VQA benchmarks.

## Key Contributions

- VISTA-Gym: unified training environment for tool-integrated VLM reasoning with verifiable feedback and trajectory logging
- Standardized visual tool interface (grounding, parsing) enabling scalable multi-turn RL
- VISTA-R1: end-to-end RL training that teaches VLMs to interleave tool calls with multi-step reasoning
- 9.51%–18.72% improvement over baselines at 8B scale across 11 VQA benchmarks

## Relevance

Hits four core profile keywords simultaneously: agentic RL, tool use, VLM, and LLM agent. This is a direct counterpart to the GUI agent survey and ERA papers from previous digests, extending tool-integrated agentic RL to general visual reasoning tasks rather than a single domain.

## My Thoughts

<!-- Add your own notes here -->
