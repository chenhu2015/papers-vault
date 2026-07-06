---
title: "Nemotron-Cascade 2: Post-Training LLMs with Cascade RL and Multi-Domain On-Policy Distillation"
authors: ["Zhuolin Yang", "Zihan Liu", "Yang Chen", "Wenliang Dai", "Boxin Wang", "Sheng-Chieh Lin", "Chankyu Lee", "Yangyi Chen", "Dongfu Jiang", "Jiafan He", "Renjie Pi", "Grace Lam", "Nayeon Lee", "Alexander Bukharin", "Mohammad Shoeybi", "Bryan Catanzaro", "Wei Ping"]
date: 2026-03-19
arxiv_id: "2603.19220v2"
url: "http://arxiv.org/abs/2603.19220v2"
score: 0.82
topics: [agentic RL, RL training, RLAIF, LLM agent, GRPO]
status: unread
---

# Nemotron-Cascade 2: Post-Training LLMs with Cascade RL and Multi-Domain On-Policy Distillation

## Summary

Nemotron-Cascade 2 is a 30B MoE model (3B activated) that reaches IMO/IOI/ICPC gold medal-level performance through two post-training innovations: Cascade RL expanded across reasoning and agentic domains, and multi-domain on-policy distillation from the strongest intermediate teacher checkpoint for each domain throughout the Cascade RL process to recover benchmark regressions. The multi-domain distillation mechanism is structurally the industrial-scale instantiation of MOPD's per-domain teacher pipeline, with Cascade RL serving as the outer training loop within which distillation from intermediate teachers operates as a continuous correction signal rather than a final-stage step.

## Key Contributions

- Cascade RL extended to a much broader spectrum of reasoning and agentic domains beyond the original Nemotron-Cascade 1 scope
- Multi-domain on-policy distillation from the strongest intermediate teacher model for each domain throughout training — not just at the end — enabling efficient recovery of benchmark regressions as new RL domains are added
- 30B MoE (3B active) achieving gold medal-level performance on IMO 2025, IOI, and ICPC World Finals, second open-weight model to do so (after DeepSeekV3.2-Special-671B-A37B), with 20× fewer parameters
- Open model weights and training data released

## Relevance

This directly instantiates MOPD (Jul 5)'s per-domain RL teacher → on-policy distillation architecture at industrial scale, adding the key insight that distillation should happen *throughout* Cascade RL (not just at the end) as a regression-correction mechanism. The intermediate-checkpoint-as-teacher strategy answers MOPD's open question about when to stop domain teacher training: train until regression appears, then distill from that intermediate checkpoint.

## My Thoughts

<!-- Add your own notes here -->
