---
title: "Rethinking Generalization in Reasoning SFT: A Conditional Analysis on Optimization, Data, and Model Capability"
authors: ["Qihan Ren", "Peng Wang", "Ruikun Cai", "Shuai Shao", "Dadi Guo", "Yuejin Xie", "Yafu Li", "Quanshi Zhang", "Xia Hu", "Jing Shao", "Dongrui Liu"]
date: 2026-04-08
arxiv_id: "2604.06628v2"
url: "https://arxiv.org/abs/2604.06628"
score: 0.82
topics: [RL training, agentic RL, RLAIF, LLM agent]
status: unread
---

# Rethinking Generalization in Reasoning SFT: A Conditional Analysis on Optimization, Data, and Model Capability

## Summary

This study challenges the SFT-memorizes/RL-generalizes narrative by showing SFT cross-domain generalization is conditional on model capability, data quality, and optimization dynamics: stronger models internalize transferable procedural patterns even from toy arithmetic, while weaker models imitate surface verbosity, and extended training reveals a dip-and-recovery pattern where early cross-domain degradation reverses. Critically, SFT generalizes reasoning while degrading safety, reframing the question as under what conditions and at what cost.

## Key Contributions

- Identifies a dip-and-recovery pattern in SFT cross-domain generalization: early degradation reverses with extended training, so short-training checkpoints underestimate generalization
- Shows data quality and structure matter independently: low-quality solutions broadly hurt generalization; verified long-CoT traces yield consistent cross-domain gains
- Demonstrates that model capability is the key determinant: stronger models internalize transferable procedural patterns while weaker models imitate surface verbosity
- Documents asymmetric generalization: SFT improves reasoning transfer while degrading safety, reframing "does SFT generalize?" as "under what conditions and at what cost?"

## Relevance

This paper directly addresses the Atomic Skills thread that has been queued for reformulation since Aug 17. The Atomic Skills Prerequisite paper (Aug 17) established that RL synthesis requires pre-mastered atomic skills; this paper establishes the parallel condition for SFT: generalization requires sufficient model capability and high-quality data. Together they form a two-sided boundary condition: SFT generalizes when the model is strong enough and data is verified; RL synthesizes when atomic skills are already present.

## My Thoughts

<!-- Add your own notes here -->
