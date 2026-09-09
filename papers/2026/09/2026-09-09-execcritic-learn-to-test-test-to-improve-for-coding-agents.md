---
title: "ExecCritic: Learn to Test, Test to Improve for Coding Agents"
authors: ["Leitian Tao", "Baolin Peng", "Haorui Wang", "Hang Wang", "Hao Cheng", "Wenlin Yao", "Qianhui Wu", "Tao Ge", "Sharon Li", "Jianfeng Gao"]
date: 2026-09-09
arxiv_id: "2609.09133v1"
url: "http://arxiv.org/abs/2609.09133v1"
score: 0.82
topics: [agentic RL, RL training, LLM agent, reward model, tool use]
status: unread
---

# ExecCritic: Learn to Test, Test to Improve for Coding Agents

## Summary

ExecCritic introduces a test-verify-revise scaffold with role-specific RL training for coding agents: a Test agent learns to produce behaviorally valid tests (Learn to Test), and a Repair agent learns source-code revision from execution feedback (Test to Improve), trained separately on Qwen-3.5-35B-A3B. The scaffold separates test construction from repair — a fail-closed harness qualifies and freezes tests before the Repair agent acts. Composing both post-trained agents reaches 72.6% on SWE-bench Verified, an 11.4-point gain over a no-test baseline without stronger-model or oracle feedback.

## Key Contributions

- Identifies that agent-generated tests can encode incorrect behavioral targets and create false confidence when the same trajectory writes both patch and test
- Test agent trained to generate behaviorally valid tests that distinguish correct from incorrect patches (Learn to Test)
- Repair agent trained with direct task resolution and feedback-guided revision from frozen, qualified test execution (Test to Improve)
- Role-specific RL: Test agent's Base-to-Gold success improves from 22.2% to 62.2%; combined post-trained agents reach 72.6% on SWE-bench Verified (+11.4pp over no-test baseline)

## Relevance

Advances the agentic RL thread by introducing role specialization (Test vs. Repair) as a structural approach to multi-step code repair — complementary to the multi-turn credit assignment papers (TRIAL, SAO, T-STAR) found Sep 08, but working at a different granularity: instead of redistributing credit within a trajectory, ExecCritic separates the trajectory into structurally distinct roles trained with different objectives. This is the execution-artifact credit thread from the open gaps list (structured credit from test outputs), approached from a role-specialization angle.

## My Thoughts

<!-- Add your own notes here -->
