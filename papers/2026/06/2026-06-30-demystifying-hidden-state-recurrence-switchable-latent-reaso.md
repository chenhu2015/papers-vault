---
title: "Demystifying Hidden-State Recurrence: Switchable Latent Reasoning with On-Policy Reinforcement Learning"
authors: ["Jiayu Yang", "Chao Chen", "Shengen Wu", "Yinhong Liu", "Yuxuan Fan", "Lujundong Li", "Songning Lai", "Chengwei Qin", "Zhijiang Guo"]
date: 2026-06-30
arxiv_id: "2606.13106"
url: "http://arxiv.org/abs/2606.13106v1"
score: 0.80
topics: [RL training, GRPO, agentic RL, LLM agent]
status: unread
---

# Demystifying Hidden-State Recurrence: Switchable Latent Reasoning with On-Policy Reinforcement Learning

## Summary

Latent chain-of-thought compresses reasoning via continuous hidden-state recurrence but is incompatible with standard on-policy RL because the GRPO policy ratio is undefined over continuous latent transitions. SWITCH introduces discrete boundary tokens (<swi></swi>) that mark latent block entry and exit, making the policy ratio well-defined at every decision point and enabling mechanistic probing of latent computation. Mechanistic analysis reveals the switch token is a sharply localized learned switching policy, the latent step performs causally important problem-specific computation concentrated at a single hidden-state transition, directly echoing ReasonMaxxer's finding that RL intervention concentrates at high-entropy branching positions.

## Key Contributions

- Discrete boundary tokens (<swi></swi>) make hidden-state recurrence compatible with GRPO by providing well-defined policy ratio anchor points
- Switch-GRPO objective propagates gradients through recurrent latent computation via a visible-to-latent curriculum
- Mechanistic finding: <swi> is a sharply localized learned switching policy, not a stylistic artefact; computation concentrated at single hidden-state transition on entry
- Outperforms prior hidden-state-recurrence approaches at similar scale while enabling direct causal intervention

## Relevance

SWITCH provides the mechanistic bridge between ReasonMaxxer (Jun 20, RL modifies 1-3% of tokens at high-entropy branching points) and latent reasoning: the <swi> boundary token IS the explicit form of that high-entropy branching position, made discrete and trainable. ProFIL (Jun 20) used a frozen-base probe to detect the commitment point in visible reasoning; SWITCH makes the commitment point structurally explicit as a learned token. The finding that latent computation concentrates at a single hidden-state transition also supports the credit assignment hierarchy: all effective RL intervention, whether in visible reasoning (ReasonMaxxer/AT-RL) or latent reasoning (SWITCH), is spatially concentrated at discrete commitment moments.

## My Thoughts

<!-- Add your own notes here -->
