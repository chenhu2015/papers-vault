---
title: "KV-PRM: Efficient Process Reward Modeling via KV-Cache Transfer for Multi-Agent Test-Time Scaling"
authors: ["Peng Kuang", "Haibo Jin", "Xiaoyu Han", "Yanli Wang", "Xiaopeng Yuan", "Ye Yu", "Kaidi Xu", "Haohan Wang"]
date: 2026-07-10
arxiv_id: "2607.09153"
url: "https://arxiv.org/abs/2607.09153"
score: 0.85
topics: [reward model, agentic RL, RL training, GRPO]
status: unread
---

# KV-PRM: Efficient Process Reward Modeling via KV-Cache Transfer for Multi-Agent Test-Time Scaling

## Summary

KV-PRM eliminates the quadratic text re-encoding cost of PRMs by reading the KV cache produced during LLM generation, scoring each reasoning step via a single 'verify token' appended to the existing cache. This reduces PRM scoring from O(L²) to O(L), yielding up to 5,000x FLOPs reduction and 37x latency reduction compared to text-based PRMs. The method matches or outperforms text-PRMs on MATH, GSM8K, and AIME under Beam Search, MCTS, and Weighted Voting, with a formal proof that KV cache carries strictly greater information capacity than text.

## Key Contributions

- KV-cache transfer for PRM scoring: O(L²) → O(L), 5,000x FLOPs reduction, 37x latency reduction, 34x memory reduction
- Formal proof that KV cache has strictly greater information capacity than equivalent text
- Matches/outperforms text-PRMs across Beam Search, MCTS, and Weighted Voting on MATH, GSM8K, AIME
- Enables PRMs in long multi-agent rollouts where text re-encoding was a prohibitive computational bottleneck

## Relevance

The vault has tracked PRMs as training signals (GroundedPRM, HRM, Jul 12) and RL^V as a verifier for TTS (Jul 12). KV-PRM resolves the inference efficiency bottleneck that makes PRMs impractical in long-context multi-agent rollouts — the same setting DART, ARTIST, and Turn-Level Reward operate in. This is the compute efficiency complement to GroundedPRM's accuracy story: GroundedPRM showed MCTS+tool-verification builds better PRMs; KV-PRM shows those PRMs can now run cheaply at multi-agent scale.

## My Thoughts

<!-- Add your own notes here -->
