---
title: "ViCrit: A Verifiable Reinforcement Learning Proxy Task for Visual Perception in VLMs"
authors: ["Xiyao Wang", "Zhengyuan Yang", "Chao Feng", "Yongyuan Liang", "Yuhang Zhou", "Xiaoyu Liu", "Ziyi Zang", "Ming Li", "Chung-Ching Lin", "Kevin Lin", "Linjie Li", "Furong Huang", "Lijuan Wang"]
date: 2025-06-11
arxiv_id: "2506.10128"
url: "https://arxiv.org/abs/2506.10128"
score: 0.75
topics: [VLM, multimodal, reward model, agentic RL, RL training]
status: unread
---

# ViCrit: A Verifiable Reinforcement Learning Proxy Task for Visual Perception in VLMs

## Summary

ViCrit introduces a verifiable RL proxy task for improving visual perception in VLMs: the model must localize a single subtle hallucination injected into a human-written image caption, receiving a binary exact-match reward. This formulation is simultaneously challenging and unambiguously verifiable — a gap in existing VLM RL proxy tasks that required either complex setups or weak verification signals. Training gains transfer beyond natural images to abstract image reasoning and visual math, suggesting genuine perceptual capability improvement rather than memorization.

## Key Contributions

- ViCrit Task: localize a single corrupted span (object, attribute, count, or spatial relation) in a 200-word caption given the original image — binary exact-match reward, no ambiguity
- ViCrit-Bench: category-balanced diagnostic benchmark probing perception errors across diverse image domains and error types
- Transfer to abstract image reasoning and visual math — showing the perceptual gains generalize beyond the proxy task distribution
- Addresses the fundamental scarcity of vision-centric tasks that are both challenging and unambiguously verifiable for VLM RL

## Relevance

Connects to the Jul 15 VLM RL asymmetry framework (SVR-R1, Aha Moment Revisited, VRRL): those papers showed that VLM self-correction via standard RL training requires deliberate failure-state coverage. ViCrit takes a different angle — instead of improving the training distribution, it improves the *reward signal quality* for visual perception by making the verification signal unambiguous and binary. The hallucination-localization proxy is structurally analogous to GRPO's math verifier: exact-match, no partial credit, no model-based judge.

## My Thoughts

<!-- Add your own notes here -->
