---
title: "PRM-BAS: Enhancing Multimodal Reasoning through PRM-guided Beam Annealing Search"
authors: ["Pengfei Hu", "Zhenrong Zhang", "Qikai Chang", "Shuhang Liu", "Jiefeng Ma", "Jun Du", "Jianshu Zhang", "Quan Liu", "Jianqing Gao", "Feng Ma", "Qingfeng Liu"]
date: 2025-04-14
arxiv_id: "2504.10222"
url: "https://arxiv.org/abs/2504.10222"
score: 0.78
topics: [VLM, multimodal, vision-language, process reward, reward model]
status: unread
---

# PRM-BAS: Enhancing Multimodal Reasoning through PRM-guided Beam Annealing Search

## Summary

PRM-BAS introduces PRM-guided Beam Annealing Search for multimodal reasoning, dynamically narrowing beam width from broad to narrow as contextual information accumulates during generation. It contributes PRM-BAS-300K, a 300K-sample multimodal dataset built via step-level rollout probability estimation, trained with a combined value loss (absolute action quality) and rank loss (relative action quality). The result is a plug-and-play lightweight approach that significantly improves MLLM reasoning across benchmarks while maintaining low computational cost and strong generalization across model scales and architectures.

## Key Contributions

- Beam Annealing Search: start broad (high beam width) and gradually narrow as step context accumulates — balances exploration at uncertain early steps with efficiency at later steps
- PRM-BAS-300K: 300K multimodal step-level dataset using rollout probability estimation for PRM supervision signal
- Combined training objective: value loss for absolute step quality + rank loss for relative step quality ordering
- Plug-and-play: generalizes across model scales and architectures without task-specific tuning

## Relevance

Directly closes the multimodal PRM gap tracked since Nov 20's digest. While Athena-PRM (Nov 21) uses consistency between weak/strong completers for PRM supervision, PRM-BAS uses rollout probability estimation — a complementary data construction approach. Together they represent two distinct multimodal PRM training strategies. PRM-BAS is older (April 2025) and surfaced via the Athena-PRM adjacent test-time scaling probe.

## My Thoughts

<!-- Add your own notes here -->
