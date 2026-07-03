---
title: "Keep Policy Gradient in Charge: Sibling-Guided Credit Distillation for Long-Horizon Tool-Use Agents"
authors: ["Tianyu Ding", "Jianhong Xin", "Juan Pablo De la Cruz Weinstein"]
date: 2026-06-10
arxiv_id: "2606.12634v2"
url: "http://arxiv.org/abs/2606.12634v2"
score: 0.85
topics: [agentic RL, tool use, GRPO, LLM agent]
status: unread
---

# Keep Policy Gradient in Charge: Sibling-Guided Credit Distillation for Long-Horizon Tool-Use Agents

## Summary

SGCD addresses a failure mode of direct self-distillation for tool-use RL: rehearsing teacher behavior without identifying which actions the verifier rewards destroys tool use. An external LLM summarizes the contrast between successful and failed sibling rollouts into a training-only credit reference, and detached teacher/student divergence reshapes GRPO token advantages while the deployed student receives only the clean task prompt. Evaluated on AppWorld and tau^3-airline, establishing that distillation should guide credit but policy gradient should drive the actor update.

## Key Contributions

- Diagnosis of direct self-distillation failure for tool-use RL: rehearsing teacher behavior without verifier-aligned credit selection collapses tool-use competence
- Sibling-Guided Credit Distillation: mixed successful/failed sibling rollouts → external LLM contrast summary → training-only credit reference that reshapes GRPO token advantages via detached divergence
- Deployment isolation: student receives only the clean task prompt; the credit reference exists only at training time, ensuring no inference overhead
- Narrow design rule supported empirically: distillation for credit guidance only; policy gradient retains exclusive authority over actor parameters

## Relevance

SGCD is CRAFT's (Jul 2) architectural cousin for tool-use environments: both use sibling rollouts as the counterfactual signal source, but where CRAFT reweights sibling tokens within the GRPO group via importance weights, SGCD offloads the contrast summarization to an external LLM to produce a cleaner credit signal for long-horizon AppWorld/tau^3 tasks where per-token importance weights may be too noisy. SGCD also addresses the same channel contamination problem PASS (Jul 1) diagnosed at the process signal input layer — but from the distillation channel rather than the PRM channel.

## My Thoughts

<!-- Add your own notes here -->
