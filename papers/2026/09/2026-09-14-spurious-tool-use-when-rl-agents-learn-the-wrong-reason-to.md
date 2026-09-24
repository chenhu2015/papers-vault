---
title: "Spurious Tool Use: When RL Agents Learn the Wrong Reason to Act"
authors: ["Yiwei Yang", "Haoxiang Zhang", "Bingbing Wen", "Yao Lu", "Yuchen Wu", "Lei Zhang", "Julian McAuley", "Pan Lu", "Bill Howe"]
date: 2026-09-14
arxiv_id: "2609.16268v1"
url: "https://arxiv.org/abs/2609.16268"
score: 0.87
topics: [agentic RL, tool use, LLM agent, reward model, RLAIF]
status: unread
---

# Spurious Tool Use: When RL Agents Learn the Wrong Reason to Act

## Summary

Studies shortcut tool-selection in RL-trained LLM agents: agents learn to invoke tools based on superficial prompt cues rather than genuine task requirements, with spurious invocation rates increasing by up to 39% when cues are present but tools are causally unnecessary. Shortcut formation emerges only once the agent has already mastered the target tool, implicating task competence as the key driver. Introducing a dense, decision-level tool-necessity reward (LLM-as-judge on each tool call) effectively suppresses cue-driven invocations while preserving task performance.

## Key Contributions

- Controlled synthetic benchmark isolating tool-use shortcut behavior in RL-trained agents across factual QA and math tasks
- Finding: task competence (not dataset imbalance alone) is the key driver of shortcut formation — shortcuts only appear after the tool is reliably learned
- Swapped-cue analysis showing semantic alignment between cue and tool substantially amplifies shortcut learning
- Dense tool-necessity reward (LLM judge on each call) as a practical mitigation: suppresses spurious calls without hurting task accuracy

## Relevance

Directly relevant to the agentic RL + tool use thread. The finding that competence enables shortcuts has implications for MATCH-style curriculum design — graduating to a new tool may create a window where the agent is vulnerable to spurious correlations. The tool-necessity reward also extends the reward model design thread, complementing EAPO's difficulty-aware reward shaping.

## My Thoughts

<!-- Add your own notes here -->
