---
title: "Verifier-Grounded Agentic RL for Provably Correct Code"
authors: ["George Ma", "Yuhao Zhang", "Bing He", "Zeren Shui", "Ferhat Erata", "Murali Krishna Ramanathan", "Somayeh Sojoudi", "Hao Zhou"]
date: 2026-10-13
arxiv_id: "2610.19298v1"
url: "http://arxiv.org/abs/2610.19298v1"
score: 0.83
topics: [agentic RL, reward model, LLM agent, reinforcement learning, GRPO]
status: unread
---

# Verifier-Grounded Agentic RL for Provably Correct Code

## Summary

Replaces binary pass/fail test-execution rewards with a graded formal verifier reward that scores candidates by weighted fraction of proof obligations discharged, augmented with hidden integrity probes to block specification gaming. Applied as a multi-turn agentic environment with a frozen proof-specialist collaborator, the method raises verification rate from 66.1% to 93.5% on DafnyBench and SWE-bench repository patch resolution from 59.6% to 72.5% across Qwen3 models.

## Key Contributions

- Formal verifier as RL reward: grades by weighted fraction of proof obligations discharged (not binary), extending the reward surface for hard problems
- Integrity audit rejects candidates that assume what they should prove, eliminating a key gaming pathway
- Frozen proof-specialist collaborator for hard verification steps during multi-turn agentic interaction
- 59.6%→72.5% SWE-bench repository patch resolution across Qwen3 1.7B to 35B MoE; graded reward leads all training signals including binary counterpart

## Relevance

Extends the SWE/code-agent RL thread (opened Nov 4 with Athanor, RSI-Dojo, Priming Base Models, SWE-Critix) with a qualitatively different reward design angle: formal verification rather than test execution. The graded-obligation-discharge approach is a direct answer to the verifier-gaming problem and complements SWE-Critix's trajectory verifier approach.

## My Thoughts

<!-- Add your own notes here -->
