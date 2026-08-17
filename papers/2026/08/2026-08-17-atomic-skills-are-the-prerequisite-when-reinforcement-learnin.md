---
title: "Atomic Skills are the Prerequisite: When Reinforcement Learning Synthesizes Compositional Reasoning, and When It Only Amplifies"
authors: ["Sitao Cheng", "Xunjian Yin", "Ruiwen Zhou", "Yuxuan Li", "Xinyi Wang", "Liangming Pan", "William Yang Wang", "Victor Zhong"]
date: 2026-08-17
arxiv_id: "2512.01970v3"
url: "http://arxiv.org/abs/2512.01970v3"
score: 0.79
topics: [agentic RL, RL training, RLHF, reward model]
status: unread
---

# Atomic Skills are the Prerequisite: When Reinforcement Learning Synthesizes Compositional Reasoning, and When It Only Amplifies

## Summary

Using controlled synthetic biographies, this paper shows RL synthesizes genuinely novel composite reasoning strategies (not just amplifies existing ones)—but only when atomic component skills are already mastered via SFT; without this prerequisite, RL achieves 90% on seen compositions but collapses to 18% on novel ones. The finding directly formalizes when capability expansion (vs. reliability improvement) occurs under RL, providing the prerequisite condition missing from PASS@(k,T)'s capability-expansion framing. It also operationalizes the atomic-skill threshold that Skill Entropy measures: RL's compositional synthesis benefit turns on exactly when per-skill entropy is low (atomic skills are stable).

## Key Contributions

- Controlled contamination-free setup: synthetic biography corpus isolates compositional task performance from pre-training data overlap
- SFT collapses on novel facts/paths (18%) despite 90% accuracy on seen facts — rote memorization not skill integration
- RL bridges the generalization gap but only under atomic skill prerequisite: decoupled SFT on atomic skills first, then RL on composite task
- Formalizes the synthesis/amplification boundary: RL is a synthesizer on unknown compositions, amplifier on known ones

## Relevance

Directly connects three vault threads: (1) Skill Entropy (Aug 16) — the formal complexity threshold is operationalized here as the prerequisite condition for RL synthesis; (2) PASS@(k,T) (Aug 16) — capability expansion vs. reliability improvement is explained by whether atomic prerequisites are met; (3) the broader credit assignment question — RL can only attribute credit to skill-switching if per-skill signal is already clean enough. The finding suggests that Skill-Entropy RL's 34.4%→68.4% gain may depend on the base model already having mastered per-skill atomic competencies.

## My Thoughts

<!-- Add your own notes here -->
