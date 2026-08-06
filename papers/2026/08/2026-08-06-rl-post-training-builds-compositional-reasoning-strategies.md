---
title: "RL Post-Training Builds Compositional Reasoning Strategies"
authors: ["Azwar Abdulsalam", "Nishil Patel", "Andrew Saxe"]
date: 2026-08-06
arxiv_id: "2607.07646"
url: "https://arxiv.org/abs/2607.07646"
score: 0.80
topics: [RL training, agentic RL, RLAIF]
status: unread
---

# RL Post-Training Builds Compositional Reasoning Strategies

## Summary

This paper provides a controlled mechanistic study of RL post-training in a fully observable grammar rewrite environment where pretraining and RL distributions are cleanly disentangled, asking whether RL amplifies latent primitives or composes new strategies. RL post-training solves held-out problems unsolvable by the base model even under large sampling budgets, while rejection fine-tuning plateaus; trace analysis reveals RL reorganizes primitive skills through a phased mechanism—first strengthening reductions, then discovering sequential and parallel compositions that are reused and consolidated. The key difference from RFT is not exploration volume but selectivity: RL concentrates exploration into valid, reusable compositional structure rather than shortcut-like rewrites.

## Key Contributions

- Fully observable, controllable rewrite grammar environment enables clean separation of pretraining vs. RL distribution
- RL post-training genuinely composes new strategies: sequential compositions (ordered chains of primitive contractions) and parallel compositions (simultaneous independent contractions) not present in pretraining
- Contrast with RFT: same exploration volume, but RL is selective (valid reusable structure), RFT is not (many shortcut/invalid rewrites)
- Pretraining ablations show compositional emergence is gated by whether pretraining organizes primitives into reduction procedures, not by primitive exposure alone

## Relevance

This paper provides mechanistic grounding for a core assumption of the vault's agentic RL thread: that RL post-training does more than amplify latent skills. The Skill-α (Aug 5) and SPyCE (Aug 3) papers treat skill composition as something that must be explicitly engineered; this paper shows RL's selectivity property naturally discovers compositional structure. The phased compositional mechanism — strengthen primitives first, then combine — mirrors the SkillRise evolution trajectory and suggests the skill lifecycle synthesis may be partly redundant with what vanilla RL already discovers in simpler environments.

## My Thoughts

<!-- Add your own notes here -->
