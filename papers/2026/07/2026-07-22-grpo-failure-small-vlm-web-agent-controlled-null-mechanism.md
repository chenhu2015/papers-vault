---
title: "A Learning-Rate-Gated Failure of GRPO in a Small Language and Vision-Language Model Web Agent: A Controlled Null and Its Mechanism"
authors: ["Chengguang Gan", "Zhixi Cai", "Yunhao Liang", "Hanjun Wei", "Shiwen Ni", "Qinghao Zhang"]
date: 2026-07-14
arxiv_id: "2607.12640"
url: "https://arxiv.org/abs/2607.12640"
score: 0.79
topics: [agentic RL, GRPO, LLM agent, VLM, vision-language, multimodal]
status: unread
---

# A Learning-Rate-Gated Failure of GRPO in a Small Language and Vision-Language Model Web Agent: A Controlled Null and Its Mechanism

## Summary

A controlled 18-run grid study (learning rate, KL weight, seed, initialization, clipping) finds that GRPO provides no credible benefit and actively degrades performance when applied to a 4–8B VLM web agent on tasks the supervised baseline has largely mastered; the key mechanistic insight is that GRPO only helps when there is "headroom" (sampling success > greedy success), confirmed by a +22-point gain when headroom exists. Grafting experiments localize the degrade regime to attention and MLP blocks, while the collapse regime cannot be traced to any single component; effective rank in late layers tracks capability at 4B but decouples at 8B, making the coupling scale-dependent. The paper provides a principled diagnostic for when to apply GRPO to agentic tasks: check whether sampling outperforms greedy at the current checkpoint before training.

## Key Contributions

- Controlled 18-run null study across learning rate, KL weight, seed, initialization, and clipping axes with paired testing and 25 evaluation seeds
- "Headroom" principle: GRPO success correlates with whether sampling success exceeds greedy success; when headroom exists, +22 pp gain with a paired interval excluding zero
- Double dissociation: degrade regime (moderate LR) localizable to attention and MLP blocks via grafting; collapse regime (high LR) not localizable to any single component
- Scale-dependent effective rank coupling: effective rank in late layers tracks capability bidirectionally at 4B but decouples at 8B

## Relevance

Provides mechanistic grounding for when GRPO fails on agentic tasks, directly complementing BPO's positive result (today). The headroom principle is a practical diagnostic that connects to CoBA-RL's capability-oriented budget allocation: both identify that the value of RL training is conditional on the model's current capability state. The VLM web agent setting (Set-of-Marks screenshot observations) makes this the first paper in the vault to study GRPO failure modes specifically in the multimodal web agent context, extending the GRPO failure analysis from reasoning-only to tool-use + visual understanding settings.

## My Thoughts

<!-- Add your own notes here -->
