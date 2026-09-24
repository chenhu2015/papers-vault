---
title: "Learning When Not to Act: Mitigating Tool Abuse in Agentic Reinforcement Learning"
authors: ["Liuji Chen", "Dianxing Tang", "Xing Shi", "Dingshuo Chen", "Qiang Liu", "Shu Wu", "Liang Wang"]
date: 2026-06-01
arxiv_id: "2606.02132v2"
url: "https://arxiv.org/abs/2606.02132"
score: 0.83
topics: [agentic RL, GRPO, tool use, reward model, LLM agent]
status: unread
---

# Learning When Not to Act: Mitigating Tool Abuse in Agentic Reinforcement Learning

## Summary

EAPO (Efficient Agentic Policy Optimization) introduces tool-free trajectories into each GRPO rollout group and applies difficulty-aware reward shaping that penalizes redundant tool calls primarily on easier queries, combined with confidence-aware token reweighting. Across nine math and knowledge-intensive benchmarks on three model families, EAPO improves over GRPO by 7–10% in average accuracy while reducing average tool calls by 18–25%.

## Key Contributions

- Tool-free trajectory injection into GRPO rollout groups: the group explicitly contains no-tool rollouts as a reference, making the policy contrast tool-use benefit directly
- Difficulty-aware reward shaping: penalizes redundant calls on easier queries where internal reasoning suffices; spares harder queries where tools genuinely help
- Confidence-aware token reweighting for improved policy gradient quality
- +7–10% accuracy over GRPO across Qwen2.5-3B/7B and Llama3.1-8B with −18–25% tool calls

## Relevance

Closely paired with the "Spurious Tool Use" paper found today: EAPO provides the training-side mitigation (reward shaping to discourage unnecessary tool use) while Spurious Tool Use diagnoses the failure mode (spurious cue-tool correlations) and proposes a complementary decision-level reward. Together they frame a complete picture of tool-use RL pathologies and fixes.

## My Thoughts

<!-- Add your own notes here -->
