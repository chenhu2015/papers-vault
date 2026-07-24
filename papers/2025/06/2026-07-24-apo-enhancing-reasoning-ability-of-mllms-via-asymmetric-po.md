---
title: "APO: Enhancing Reasoning Ability of MLLMs via Asymmetric Policy Optimization"
authors: ["Minjie Hong", "Zirun Guo", "Yan Xia", "Zehan Wang", "Ziang Zhang", "Tao Jin", "Zhou Zhao"]
date: 2026-07-24
arxiv_id: "2506.21655"
url: "http://arxiv.org/abs/2506.21655v1"
score: 0.82
topics: [multimodal models, VLM, vision-language, RLHF, GRPO, reward model]
status: unread
---

# APO: Enhancing Reasoning Ability of MLLMs via Asymmetric Policy Optimization

## Summary

APO identifies that KL penalty dynamics and overthinking are the two main obstacles to RL in multimodal LLMs, and proposes asymmetric treatment of positive and negative responses. For positive samples, DADS dynamically scales the KL divergence weight by response difficulty to prevent entropy collapse; for negative samples, STCR penalizes over-long responses to suppress overthinking while preserving exploration. View-R1-3B (Qwen2.5-VL-3B + APO) achieves 7% average gain over the base model and outperforms 7–11B MLLMs on reasoning benchmarks without degrading general task performance.

## Key Contributions

- DADS (Difficulty-Adaptive Divergence Shaping): dynamically adjusts KL divergence weight for positive samples based on difficulty — lower penalty on hard positives to allow more exploration, higher on easy positives to preserve existing knowledge
- STCR (Suboptimal Trajectory Complexity Regularization): penalizes overly long negative responses, mitigating overthinking while maintaining exploration capacity
- Asymmetric design applies different optimization objectives to correct vs. incorrect trajectories at the KL/complexity level, not just at the advantage sign level
- View-R1-3B: 3B model outperforms 7–11B MLLMs while maintaining general task performance, demonstrating the parameter-efficiency of asymmetric treatment

## Relevance

APO closes the persistent open gap on asymmetric correct/incorrect response treatment (confirmed sparse, gap item #7 since Jul 15). Where DISPO's asymmetric IS clipping operates at the importance weight level and GFlowRL's flow-gap clipping operates at the trajectory deviation level, APO operates at the KL divergence and trajectory length level — a structurally distinct intervention point. The multimodal setting directly addresses the VLM RL axis: APO is the first vault paper to study how KL penalty dynamics differ between visual reasoning positives and negatives specifically, connecting to the VLM RL faithfulness thread (FWS, CORA, SIVA-RL, DyCo-RL) via the entropy collapse mechanism.

## My Thoughts

<!-- Add your own notes here -->
