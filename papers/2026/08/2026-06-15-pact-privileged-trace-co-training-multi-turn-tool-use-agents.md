---
title: "PACT: Privileged Trace Co-Training for Multi-Turn Tool-Use Agents"
authors: ["Zhenbang Du", "Jun Luo", "Zhiwei Zheng", "Xiangchi Yuan", "Kejing Xia", "Dachuan Shi", "Qirui Jin", "Qijia He", "Shaofeng Zou", "Yingbin Liang", "Wenke Lee"]
date: 2026-06-15
arxiv_id: "2606.16215"
url: "https://arxiv.org/abs/2606.16215"
score: 0.78
topics: [agentic RL, tool use, RL training, LLM agent]
status: unread
---

# PACT: Privileged Trace Co-Training for Multi-Turn Tool-Use Agents

## Summary

PACT uses expert traces only as training-time optimization signals while keeping rollout generation entirely prompt-only, decoupling the dense supervision benefit of SFT from the trajectory-overconstraint cost. Two complementary signals are injected: a trace-conditioned RL surrogate that scores prompt-only rollouts in the context of expert traces, and a component-aware SFT loss with annealed strength targeting reasoning prefixes and tool-call structure. PACT consistently outperforms strong SFT- and RL-based baselines on FTRL, BFCL, and ToolHop benchmarks for multi-turn tool-use agents.

## Key Contributions

- Privileged trace decoupling: expert traces used only at training (optimization signal), never at rollout — inference remains prompt-only
- Trace-conditioned RL surrogate: evaluates prompt-only rollouts under expert-trace context, getting dense guidance without trajectory constraint
- Component-aware SFT loss: annealed supervision targeting reasoning prefixes and tool-call components (not the entire trace), reducing over-imitation
- Prompt-only anchoring loss to prevent over-reliance on trace context

## Relevance

Connects to two vault threads: (1) the experience internalization cluster (EDGE, Evolving-RL, Aug 27) — all three try to benefit from demonstrations/experience at training time without inference-time scaffolds; PACT uses expert traces, EDGE uses self-generated experience. (2) The SFT-conflicts-RL-coexists papers (Aug 5, 20) on when SFT and RL objectives interfere. PACT's annealed SFT component is a practical answer to that tension: reduce SFT signal progressively as RL takes hold.

## My Thoughts

<!-- Add your own notes here -->
