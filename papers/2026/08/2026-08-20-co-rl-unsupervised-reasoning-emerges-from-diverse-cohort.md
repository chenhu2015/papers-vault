---
title: "Co-RL: Unsupervised Reasoning Emerges from Diverse Cohort in Multi-agent RL"
authors: ["Yunhao Yang", "Yuexin Bian", "Yunjie Tian", "Di Fu", "Tianjin Huang", "Yuanyuan Shi", "Ziang Xiao", "Nuno Vasconcelos", "Yijiang Li"]
date: 2026-08-18
arxiv_id: "2608.17253"
url: "https://arxiv.org/abs/2608.17253"
score: 0.88
topics: [RLAIF, RL training, multimodal models, VLM, agentic RL]
status: unread
---

# Co-RL: Unsupervised Reasoning Emerges from Diverse Cohort in Multi-agent RL

## Summary

Multiple decoupled LLM/VLM models are simultaneously RL-trained using reward signals derived from peer completions rather than ground-truth labels, removing the need for human annotations or verifiable rewards. Increasing cohort diversity across model families, sizes, and rephrased training samples breaks correlated error feedback loops, maintaining behavioral diversity and preventing training collapse. Co-RL matches or surpasses supervised RL across seven text-only and four multimodal benchmarks, demonstrating scalable unsupervised RLAIF for both LLMs and VLMs.

## Key Contributions

- Peer-reward mechanism: each model in the cohort receives RL reward derived from agreement/disagreement with other models' completions, not from ground truth
- Diversity hypothesis: heterogeneous model families and sizes break correlated error loops that cause self-rewarding collapse in single-model self-improvement
- Extends to VLMs: 2.3–7.2% gains on multimodal benchmarks alongside 3.0–8.6% on text-only, establishing VLM-parity with LLM scaling behavior
- Competitive with supervised RL on reasoning benchmarks without any ground-truth annotation access

## Relevance

This directly addresses the supervision bottleneck in RLAIF — the vault's RL papers (GUPO, GRPO multilingual, on-policy distillation) all assume verifiable reward signals. Co-RL shows the peer-cohort reward can substitute for ground truth, which is particularly relevant for the VLM domain where verifiable rewards are scarce and the interest profile's RLAIF and VLM keywords both apply.

## My Thoughts

<!-- Add your own notes here -->
