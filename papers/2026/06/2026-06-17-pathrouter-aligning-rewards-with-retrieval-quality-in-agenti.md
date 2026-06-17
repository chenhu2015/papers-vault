---
title: "PathRouter: Aligning Rewards with Retrieval Quality in Agentic Graph Retrieval-Augmented Generation"
authors: ["Bo Wang", "Heyan Huang", "Yaolin Li", "Wei Tang", "Yuan Zhang", "Wenbo Li", "Mingze Gao", "Ge Shi", "Chong Feng"]
date: 2026-06-15
arxiv_id: "2606.16409v1"
url: "http://arxiv.org/abs/2606.16409v1"
score: 0.74
topics: [agentic RL, reward model, GRPO, LLM agent, tool use]
status: unread
---

# PathRouter: Aligning Rewards with Retrieval Quality in Agentic Graph Retrieval-Augmented Generation

## Summary

PathRouter identifies and resolves answer-path reward aliasing in agentic GraphRAG — where outcome-only GRPO reinforces shortcut paths that give correct answers without retrieving useful evidence. Jointly evaluating trajectories on answer correctness and evidence-path overlap yields four trajectory categories with differentiated GRPO advantage scaling; for evidence-poor trajectories, a frozen gold-evidence teacher provides token-level KL guidance on reasoning and search-query tokens (excluding answer tokens), achieving average F1 gains of 3.1 on 3B and 4.9 on 7B models.

## Key Contributions

- Answer-path reward aliasing: outcome-only RL reinforces shortcut retrieval paths that give correct answers via surface-level matching rather than genuine evidence
- Four trajectory categories from joint (correctness × path overlap) evaluation with differentiated GRPO advantage scaling
- Frozen gold-evidence teacher KL guidance for evidence-poor trajectories: applied to reasoning and search-query tokens only, not answer tokens (prevents imitation)
- Consistent +3.1–4.9 F1 average gains across six QA benchmarks at 3B and 7B

## Relevance

Answer-path reward aliasing is the retrieval-agent specific instance of a general problem observed across agentic RL: CVT-RL (Jun 11) showed that outcome-only reward reinforces shortcut behaviors and requires causal intervention; FORT-Searcher (Jun 11) found that shortcut-resistant training data matters more than algorithm. PathRouter is the reward-design solution in this family: instead of filtering training data (FORT-Searcher) or causal counterfactual correction (CVT-RL), it directly signals the agent on evidence quality within the reward.

## My Thoughts

<!-- Add your own notes here -->
