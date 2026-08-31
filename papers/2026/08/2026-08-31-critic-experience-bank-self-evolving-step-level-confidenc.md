---
title: "Critic Experience Bank: Self-Evolving Step-Level Confidence Estimation for LLM Agents"
authors: ["Yaopei Zeng", "Congchao Wang", "JianHang Chen", "Nan Wang", "Yurui Chang", "Lu Lin"]
date: 2026-08-31
arxiv_id: "2607.12397"
url: "https://arxiv.org/abs/2607.12397"
score: 0.76
topics: [agentic RL, RL training, LLM agent, tool use, agentic]
status: unread
---

# Critic Experience Bank: Self-Evolving Step-Level Confidence Estimation for LLM Agents

## Summary

Critic Experience Bank (CEB) addresses step-level confidence estimation for LLM agents by accumulating hindsight pseudo-labels: after each trajectory, a hindsight LLM that sees the full execution feedback votes on whether each step was productive, and these pseudo-labels populate a retrievable memory bank used at the next step decision. CEB requires no training and no ground-truth step labels, yet achieves best-in-class calibration (ECE and Brier score) and ranking (AUC) across three agent benchmarks, reducing ECE by up to 54% relative to the strongest training-free baseline.

## Key Contributions

- Hindsight pseudo-labeling: a hindsight LLM with access to the full trajectory outcome retrospectively votes on per-step productivity, bootstrapping supervision from trajectory-level outcome without dense annotations
- Memory bank: productive and unproductive experience pairs are stored and retrieved (by step similarity) into the critic's prompt at inference time
- Self-evolving without training: the bank grows and improves as the agent operates, requiring no offline dataset or training loop
- Best ECE, Brier, and AUC on three agent benchmarks (unspecified in abstract) across three critic backbone LLMs

## Relevance

CEB connects to two open threads in the vault. First, the credit assignment taxonomy (SPA-RL, MileGPO, DataPRM/ToolPRM, IAPO, EFCA — Aug 30) focuses on training-time credit; CEB is the first vault paper applying a similar hindsight mechanism at inference-time for deployment confidence rather than training signal. Second, CEB's hindsight labeling shares structural similarity with PACT (Aug 29): both use post-hoc trajectory information to generate supervision signals that were not available at rollout time.

## My Thoughts

<!-- Add your own notes here -->
