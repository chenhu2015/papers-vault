---
title: "ReLook: Vision-Grounded RL with a Multimodal LLM Critic for Agentic Web Coding"
authors: ["Yuhang Li", "Chenchen Zhang", "Ruilin Lv", "Ao Liu", "Ken Deng", "Yuanxing Zhang", "Jiaheng Liu", "Wiggin Zhou", "Bo Zhou"]
date: 2026-07-07
arxiv_id: "2510.11498v1"
url: "http://arxiv.org/abs/2510.11498v1"
score: 0.72
topics: [agentic RL, tool use, multimodal, vision-language, VLM, LLM agent, RLAIF]
status: unread
---

# ReLook: Vision-Grounded RL with a Multimodal LLM Critic for Agentic Web Coding

## Summary

ReLook targets front-end code generation where correctness is judged on rendered pixels rather than string matching, using an MLLM-in-the-loop RL design: during training, the agent invokes an MLLM as a visual critic that scores code from browser screenshots and provides vision-grounded actionable feedback. Forced Optimization enforces monotonically improving trajectories via a strict acceptance rule (only improving revisions are admitted), preventing behavioral collapse. Training-inference decoupling removes the critic at inference time, yielding a lightweight self-edit cycle at latency comparable to base decoding.

## Key Contributions

- Vision-grounded RL: MLLM as both visual critic (screenshot scoring) and feedback source during training
- Forced Optimization: strict acceptance rule requiring monotonically improving revisions, preventing collapse
- Zero-reward rule for invalid renders: anchors renderability to prevent reward hacking at code-generation boundaries
- Training-inference decoupling: critic-free inference preserves gains at base decoding latency

## Relevance

Operationalizes the RLAIF thread (MLLM as critic rather than human labeler) in the agentic tool-use domain where the reward signal is inherently visual (rendered output). Complements AutoTool (today) at a different level: AutoTool decides *whether* to invoke tools adaptively; ReLook determines *how* to iteratively refine tool output using MLLM-judged visual feedback. Together they address the two key policy decisions in agentic tool-augmented systems: invocation and revision.

## My Thoughts

<!-- Add your own notes here -->
