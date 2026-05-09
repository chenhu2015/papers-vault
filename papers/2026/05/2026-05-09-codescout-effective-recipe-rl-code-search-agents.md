---
title: "CodeScout: An Effective Recipe for Reinforcement Learning of Code Search Agents"
authors: ["Lintang Sutawika", "Aditya Bharat Soni", "Bharath Sriraam R R", "Apurva Gandhi", "Taha Yassine", "Sanidhya Vijayvargiya", "Yuchen Li", "Xuhui Zhou", "Yilin Zhang", "Leander Melroy Maben", "Graham Neubig"]
date: 2026-05-09
arxiv_id: "2603.17829v1"
url: "http://arxiv.org/abs/2603.17829v1"
score: 0.82
topics: [agentic RL, reinforcement learning, tool use, LLM agent]
status: unread
---

# CodeScout: An Effective Recipe for Reinforcement Learning of Code Search Agents

## Summary

CodeScout demonstrates that a coding agent equipped with only a standard Unix terminal can achieve competitive code localization via a carefully designed RL training recipe, without specialized tools or repository graphs. The paper contributes techniques for repurposing coding environments for code search, reward design, and RL optimization, releasing the full CodeScout model family. On SWE-Bench Verified, Pro, and Lite, CodeScout consistently outperforms base models 2–18× larger and approaches closed-source models like Claude Sonnet.

## Key Contributions

- Minimal-tool RL: terminal-only agent beats models with specialized static analysis scaffolds
- Techniques for repurposing existing coding agent environments for code search (environment re-use, reward shaping)
- RL reward design specifically for code localization (file, class, function identification)
- Open-source CodeScout model family (code and data released)

## Relevance

Directly targets the "agentic RL" and "tool use" core topics: shows that RL training recipe quality matters more than tool richness for code agents. Pairs naturally with SWE-Shepherd (also found today) which addresses reward model quality for the same code-agent setting.

## My Thoughts

<!-- Add your own notes here -->
