---
title: "Priming Base Models for Agentic Post-Training: An Open Midtraining Recipe"
authors: ["Soumye Singhal", "Joseph Jennings", "Ka Shun Shum", "Alexander Bukharin", "Khushi Bhardwaj", "Zirui Liu", "Venkat Srinivasan", "Jonathan Li", "Yash Jain", "Kezhi Kong", "Markus Kliegl", "Olivier Delalleau", "Sanjeev Satheesh", "Mostofa Patwary"]
date: 2026-10-15
arxiv_id: "2610.22019v1"
url: "http://arxiv.org/abs/2610.22019v1"
score: 0.78
topics: [agentic RL, RL training, LLM agent, agentic]
status: unread
---

# Priming Base Models for Agentic Post-Training: An Open Midtraining Recipe

## Summary

This paper presents an open midtraining recipe that sits between pretraining and SFT/RL post-training, training at 256K context for 280–500 billion tokens on a diverse mix of natural software-engineering data (packed repositories, pull requests, commit histories, build logs) plus a small share of agentic traces. On Nemotron 3.5 Lightning, 500B midtraining tokens improve SWE-bench Verified from 60.7 to 64.5 and Multilingual from 55.8 to 62.8 after identical SFT; on Nemotron 3.5 Super, 280B tokens improve DeepSWE from 11.7 to 15.7 and SWE-bench Verified from 72.9 to 74.3. Key finding: base-model proxy metrics do not reliably correlate with post-training results, motivating short fixed SFT evaluation runs as an evaluation protocol.

## Key Contributions

- Open midtraining recipe: 256K context, natural SE data (repos, PRs, commits, build logs) + small agentic trace share, between pretraining and post-training
- Consistent improvements on SWE-bench Verified, Multilingual, Pro, and DeepSWE benchmarks across two model sizes after identical full SFT
- Base-model proxy metrics do not correlate with post-training results — short fixed SFT runs are needed for reliable midtraining evaluation
- Midtraining also improves robustness across agent harnesses on both models

## Relevance

Directly relevant to the SWE/code-agent RL thread opened today: the paper provides the data and training recipe scaffolding that makes subsequent agentic RL effective. Connects to CoHARL and Athanor's finding that harness diversity and infrastructure quality matter for agentic RL outcomes.

## My Thoughts

<!-- Add your own notes here -->
