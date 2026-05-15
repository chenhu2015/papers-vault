---
title: "SPELL: Self-Play Reinforcement Learning for Evolving Long-Context Language Models"
authors: ["Ziyi Yang", "Weizhou Shen", "Chenliang Li", "Ruijun Chen", "Fanqi Wan", "Ming Yan", "Xiaojun Quan", "Fei Huang"]
date: 2025-09-28
arxiv_id: "2509.23863"
url: "https://arxiv.org/abs/2509.23863"
score: 0.80
topics: [agentic RL, RL training, reward model, reinforcement learning, LLM agent]
status: unread
---

# SPELL: Self-Play Reinforcement Learning for Evolving Long-Context Language Models

## Summary

SPELL applies multi-role self-play to long-context reasoning: a single model acts as questioner (generating questions from raw documents), responder (answering from full context), and verifier (scoring semantic equivalence for reward). An automated curriculum gradually increases document length while adapting question difficulty to model capability, enabling label-free, scalable long-context RL. The method achieves a 7.6-point pass@8 gain on the strong Qwen3-30B-A3B-Thinking baseline and consistently outperforms models fine-tuned on large annotated corpora.

## Key Contributions

- Multi-role self-play framework (questioner/responder/verifier) in a single model for long-context RL without human labels
- Automated curriculum over document length tied to model performance — length increases as capability grows
- Reward via verifier semantic equivalence check, eliminating need for hand-crafted verifiable signals
- 7.6-point pass@8 improvement on Qwen3-30B-A3B-Thinking; outperforms annotation-heavy fine-tuning baselines

## Relevance

SPELL extends the self-play thread into the long-context domain, combining it with the curriculum RL ideas from May 13's METIS/AdaCuRL/VCRL papers. The verifier-as-reward-signal approach is a concrete application of self-rewarding that avoids majority voting (compared to SeRL), using semantic equivalence instead — an interesting design choice worth noting when both papers are contrasted.

## My Thoughts

<!-- Add your own notes here -->
