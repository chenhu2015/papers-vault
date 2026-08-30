---
title: "psRL: Efficient Training for Agentic AI via Training-Time Prefix Sharing"
authors: ["Mianjie Yu", "Zizhao Mo", "Huanyu Qu", "Zhirong Qian", "Huanle Xu", "Cen Li", "Zifeng Zhao", "Zhi Zhou", "Jinhua Zhou", "Jun Xie", "Chengzhong Xu"]
date: 2026-08-30
arxiv_id: "2608.25683"
url: "https://arxiv.org/abs/2608.25683"
score: 0.71
topics: [agentic RL, RL training, LLM agent, tool use]
status: unread
---

# psRL: Efficient Training for Agentic AI via Training-Time Prefix Sharing

## Summary

Identifies that tree-structured and step-wise RL training strategies shift the system bottleneck from rollout generation to the gradient update phase due to substantial prefix redundancy across training samples, and proposes psRL—a distributed training system with two prefix-sharing mechanisms for fine-grained GPU workload distribution and a KV cache manager with adaptable block-size allocation and dynamic caching to maximize memory utilization while maintaining high prefix hit rates. Production-trace evaluations demonstrate up to 5.2× throughput improvement over existing agentic RL training systems.

## Key Contributions

- Identifies update-phase bottleneck in modern step-wise/tree-structured agentic RL as a new systems problem distinct from rollout efficiency
- Two prefix-sharing mechanisms enabling flexible workload distribution across GPU workers with simultaneous prefix reuse and load balancing
- New KV cache manager with adaptable block-size allocation for the update phase (previously KV caching was primarily used in inference)
- 5.2× throughput improvement on production traces — practical enabler for large-scale step-wise agentic RL training

## Relevance

psRL complements the algorithmic papers in the vault (SPO++, IAPO, EFCA) by addressing the infrastructure layer that makes large-scale agentic RL feasible. The bottleneck shift it identifies (rollout → update) is directly caused by the step-wise and tree-structured sampling strategies used in papers like ZeroTIR (scaling laws) and PACT (privileged traces), making psRL the first vault paper to treat these training strategies' infrastructure cost as the primary object of study.

## My Thoughts

<!-- Add your own notes here -->
