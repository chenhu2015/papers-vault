---
title: "VICT: Verifier-Instrumented Credit Tracing for Long-Horizon LLM Agent Reinforcement Learning"
authors: ["Pengcheng Li", "Zhengyang Zhang", "Dongxu Zhang", "Sui Huang", "Shaohua Ma"]
date: 2026-09-07
arxiv_id: "2608.28128v1"
url: "https://arxiv.org/abs/2608.28128"
score: 0.85
topics: [agentic RL, LLM agent, tool use, GRPO, reinforcement learning, reward model]
status: unread
---

# VICT: Verifier-Instrumented Credit Tracing for Long-Horizon LLM Agent Reinforcement Learning

## Summary

VICT reframes credit assignment in long-horizon agentic RL by exposing executable or evidence-backed atoms that already exist inside the terminal verifier and tracing them back to actions via dependency-valid proof edges. Group-relative advantage is redistributed only along those edges, shifting credit assignment from rollout-side inference to verifier-side tracing without a learned critic, process labels, branch rollouts, or inference-time verifier access. On ALFWorld and WebShop, VICT substantially outperforms outcome-only training and matches recent fine-grained credit methods while remaining orthogonal to rollout-side approaches such as OTB and DARS.

## Key Contributions

- Verifier-side credit tracing: exposes verifier-internal executable/evidence-backed atoms and traces them to actions via dependency-valid proof edges — no learned critic, process labels, or branch rollouts required
- Advantage redistribution restricted to proof edges only — preserves original terminal reward, abstains when evidence is incomplete or ambiguous
- Changes only the training-time advantage tensor; inference-time verifier access not required
- ALFWorld and WebShop: substantially outperforms outcome-only training, ablations rule out dense atom rewards, final-commit credit, temporal proximity, and sparsity as explanations

## Relevance

VICT adds a new axis to the credit assignment thread established through Sep 06: while OTB (per-token advantage reweighting from response-level variance), DARS (planner-level prefix-gated reward + token-level routing), DiDPO (code-diff-level groupability anchors), and VICT all address credit assignment, VICT is uniquely verifier-side rather than rollout-side — it extracts credit signal from the verifier's internal structure, not from trajectory comparison or rollout statistics. This makes VICT orthogonal to all prior axes and composable with them.

## My Thoughts

<!-- Add your own notes here -->
