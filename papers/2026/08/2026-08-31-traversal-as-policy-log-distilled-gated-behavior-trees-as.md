---
title: "Traversal-as-Policy: Log-Distilled Gated Behavior Trees as Externalized, Verifiable Policies for Safe, Robust, and Efficient Agents"
authors: ["Peiran Li", "Jiashuo Sun", "Fangzhou Lin", "Shuo Xing", "Tianfu Fu", "Suofei Feng", "Chaoqun Ni", "Zhengzhong Tu"]
date: 2026-08-31
arxiv_id: "2603.05517"
url: "https://arxiv.org/abs/2603.05517"
score: 0.73
topics: [agentic RL, RL training, LLM agent, agentic, tool use]
status: unread
---

# Traversal-as-Policy: Log-Distilled Gated Behavior Trees as Externalized, Verifiable Policies for Safe, Robust, and Efficient Agents

## Summary

Traversal-as-Policy distills sandboxed OpenHands execution logs into Gated Behavior Trees (GBT) — executable, human-auditable control policies where tree traversal replaces unconstrained generation whenever a task is in coverage. Nodes encode state-conditioned action macros from successful trajectories; unsafe-trace-implicated macros attach deterministic pre-execution gates that are monotonically tightened from experience. On SWE-bench Verified, GBT raises success from 34.6% to 73.6% and reduces violations from 2.8% to 0.2%; with the same distilled tree, 8B executors jump from 14.0% to 58.8%.

## Key Contributions

- Log distillation into GBTs: successful execution trajectories are mined for state-conditioned action macros; macros are merge-checked and organized into a tree structure representing the policy's known-good behavior repertoire
- Safety gating: macros implicated by unsafe traces attach deterministic pre-execution gates; gates are monotonically updated under experience-grounded constraints so previously rejected unsafe contexts cannot be re-admitted
- Runtime traversal: a lightweight traverser matches the base model's intent to child macros, executes one macro at a time, and performs risk-aware shortest-path recovery when stalled — the visited path forms a compact spine memory replacing transcript replay
- Generalization across model scales: the same GBT distilled from a large model raises 8B executor success from 14.0% to 58.8% on SWE-bench Verified — tree structure transfers across model scales

## Relevance

GBT represents a structurally distinct position in the distillation design space relative to SPT (Aug 30) and PACT (Aug 29). SPT absorbs skill knowledge into model parameters before RL; PACT uses expert traces as training-time optimization signals; GBT externalizes the distilled policy as a tree that replaces generation at runtime. The three positions are: (a) parameter absorption (SPT), (b) training-time signal (PACT), (c) runtime replacement (GBT). GBT's "coverage or generate" runtime decision also echoes EDGE (Aug 22)'s experience-distillation approach but applies the idea at the policy level rather than the exploration-guidance level.

## My Thoughts

<!-- Add your own notes here -->
