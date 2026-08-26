---
title: "Rewarding the Scientific Process: Process-Level Reward Modeling for Agentic Data Analysis"
authors: ["Zhisong Qiu", "Shuofei Qiao", "Kewei Xu", "Yuqi Zhu", "Lun Du", "Ningyu Zhang", "Huajun Chen"]
date: 2026-04-27
arxiv_id: "2604.24198v2"
url: "http://arxiv.org/abs/2604.24198v2"
score: 0.78
topics: [agentic RL, reward model, RL training, LLM agent]
status: unread
---

# Rewarding the Scientific Process: Process-Level Reward Modeling for Agentic Data Analysis

## Summary

DataPRM is an environment-aware generative PRM for agentic data analysis that distinguishes two failure modes standard PRMs miss: silent errors (incorrect results without exceptions) and exploratory actions (necessary trial-and-error wrongly penalized as grounding failures). The verifier actively interacts with the environment to probe intermediate execution states, and a reflection-aware ternary reward strategy separates correctable from irrecoverable mistakes. With only 4B parameters, DataPRM improves downstream policy LLMs by 7.21% on ScienceAgentBench and 11.28% on DABStep.

## Key Contributions

- Identifies two failure modes of standard PRMs in dynamic agentic settings: silent errors and exploratory action penalization
- Environment-aware generative verifier that actively probes intermediate execution states (not just static step evaluation)
- Reflection-aware ternary reward: distinguishes no-error, correctable-error, and irrecoverable-error
- Scalable 8K training pipeline via diversity-driven trajectory generation + knowledge-augmented step-level annotation
- Best-of-N and RL training improvements: +7.21% ScienceAgentBench, +11.28% DABStep with a 4B-param PRM

## Relevance

DataPRM extends the credit assignment thread (Credit Without Ground Truth Aug 21, Verifiable Counterfactual Supervision Aug 22) to a new task domain: agentic data analysis rather than ALFWorld/WebShop. Its "silent error" concept is the data-analysis equivalent of the causal contribution problem — a step that produces correct-looking intermediate output but is actually wrong is precisely the case where step correctness and step contribution diverge. The environment-aware verifier (actively probing execution states) is also structurally analogous to Verifiable Counterfactual Supervision's error injection approach: both construct supervision by interacting with a ground-truth environment rather than relying on static trajectory annotation.

## My Thoughts

<!-- Add your own notes here -->
