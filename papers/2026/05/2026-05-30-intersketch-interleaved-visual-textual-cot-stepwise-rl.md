---
title: "InterSketch: An Interleaved Reasoning Model with Self-correcting Visual Sketch and Stepwise Reward"
authors: ["Zhiwei Ning", "Wenwen Tong", "Xiangli Kong", "Shengnan Ma", "Ziyi Shang", "Jingcheng Ni", "Tao Hu", "Yong Xien Chng", "Jixuan Ying", "Zehuan Wu", "Hanming Deng", "Jie Yang", "Yuanjie Zheng", "Wei Liu", "Lewei Lu"]
date: 2026-05-26
arxiv_id: "2605.26520"
url: "http://arxiv.org/abs/2605.26520v1"
score: 0.82
topics: [VLM, multimodal, vision-language, reward model, RL training]
status: unread
---

# InterSketch: An Interleaved Reasoning Model with Self-correcting Visual Sketch and Stepwise Reward

## Summary

InterSketch enables interleaved visual-textual chain-of-thought by dynamically generating intermediate visual sketches with external tools and interleaving them with text reasoning across long-horizon visual tasks, then uses RL with stepwise rewards to mitigate end-only supervision sparsity. After a cold-start SFT stage with synthesized VT-CoT data and a reflection mechanism, RL with stepwise rewards further refines the policy; InterSketch outperforms proprietary models including Gemini-3-Pro on visual reasoning benchmarks.

## Key Contributions

- Interleaved VT-CoT: external tool generates visual sketches dynamically interleaved with text reasoning
- Cold-start SFT on synthesized high-quality interleaved VT-CoT data with self-correction reflection
- Stepwise RL reward mitigates reward sparsity over long-horizon visual reasoning trajectories
- Outperforms Gemini-3-Pro and strong open-source VLMs on visual reasoning benchmarks

## Relevance

Extends the multimodal agentic VLM RL carry-forward with a long-horizon interleaved visual-textual reasoning approach — distinct from the super-resolution tool-use angle of Mags-RL found today.

## My Thoughts

<!-- Add your own notes here -->
