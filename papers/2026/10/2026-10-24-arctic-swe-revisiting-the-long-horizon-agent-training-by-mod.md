---
title: "Arctic-SWE: Revisiting the Long Horizon Agent Training by Modeling-System Co-Design"
authors: ["Boyi Liu", "Yite Wang", "Xinyu Lian", "Fan Shu", "Sida Li", "Feng Yan", "Mingjia Zhang", "Yuxiong He", "Zhewei Yao"]
date: 2026-10-17
arxiv_id: "2610.24914v1"
url: "http://arxiv.org/abs/2610.24914v1"
score: 0.82
topics: [agentic RL, LLM agent, reinforcement learning, RL training]
status: unread
---

# Arctic-SWE: Revisiting the Long Horizon Agent Training by Modeling-System Co-Design

## Summary

Fully asynchronous RL framework for long-horizon software engineering agent training establishing a reproducible baseline via model-system co-design: gated reward, importance-weight control, aligned training/inference engines, consistent state across policy updates. Without new algorithms, trains Qwen3.5-4B to 62.0% on SWE-bench Verified from raw R2E-Gym data—comparable to concurrent work requiring online task synthesis at 1/6 the rollouts. Curated data subset further improves to 65.0%/38.3%/59.7% on SWE-bench Verified/Pro-v1/Pro-v2.

## Key Contributions

- Identifies that many reported gains in long-horizon agent RL come from under-tuned baselines; uses overfitting on a small task pool as a diagnostic testbed to isolate component contributions
- Model-system co-design: gated reward, importance-weight control, aligned training/inference engines, consistent state across policy updates — no single component is new, but combined they form a missing foundation
- Achieves 62.0% SWE-bench Verified at 4B scale without new algorithms or data engineering, comparable to concurrent online-synthesis methods at 1/6 the rollouts
- Controlled comparisons show both data curation and stronger tests improve held-out performance, with an important caveat: stronger tests reduce apparent training-task mastery

## Relevance

First systematic answer to the multi-turn/long-horizon agentic RL gap tracked over 3 search attempts; directly fills the thread by providing a principled infrastructure baseline for coding agent RL. Arctic-SWE's model-system co-design philosophy connects to IsoCompute's compute allocation framing: both argue that engineering hygiene (not new algorithms) explains most reported gains.

## My Thoughts

<!-- Add your own notes here -->
