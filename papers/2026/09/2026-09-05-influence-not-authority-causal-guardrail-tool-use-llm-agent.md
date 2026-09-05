---
title: "Influence Is Not Authority: When Causal Guardrail Signals Make Legitimate Tool Use Look Like an Attack in Tool-Using LLM Agents"
authors: ["Tanzim Ahad", "Ismail Hossain", "Md Jahangir Alam", "Sai Puppala", "Syed Bahauddin Alam", "Sajedul Talukder"]
date: 2026-09-05
arxiv_id: "2608.29942v1"
url: "http://arxiv.org/abs/2608.29942v1"
score: 0.73
topics: [agentic, tool use, LLM agent]
status: unread
---

# Influence Is Not Authority: When Causal Guardrail Signals Make Legitimate Tool Use Look Like an Attack in Tool-Using LLM Agents

## Summary

This paper audits influence-based guardrails for tool-using LLM agents across 96 conditions derived from 24 base cases, showing that guardrails based on causal influence signals cannot reliably distinguish legitimate, user-authorized tool calls from malicious injections when both rely on the same external tool information. Holding the committed action, its intended effect, and authorization fixed while varying only whether a required value comes from the user or a legitimate tool result shifts the causal signal toward the attack region, triggering unnecessary verification and adding latency for benign actions. This reveals a fifth failure mode in the agent faithfulness audit stack: guardrail false positives at the safety/utility boundary, complementing CTA (skill-attribution blindness), FACE-Eval (covert adoption), REDAgentBench (verbalization-execution gap), and CSR (causal step-necessity).

## Key Contributions

- Authorization-equivalence audit: 96 conditions × 24 base cases, systematically varying information source (user vs. legitimate tool result) while holding action and effect fixed
- Demonstrates that influence-based guardrails conflate causal influence with malicious authorization — a fundamental design flaw, not a tuning problem
- Identifies fifth failure mode for the agent faithfulness audit stack: guardrail false positives (benign tool use misclassified as injection attack)
- Explains the safety/utility tension: the same causal signal that catches genuine attacks also penalizes legitimate high-influence tool calls

## Relevance

This extends the agent faithfulness audit thread (FACE-Eval, REDAgentBench, CSR, CTA) in a new direction: rather than faithfulness failures internal to the agent's reasoning chain, this is a faithfulness failure in the safety infrastructure that monitors the agent. The four-failure-mode unified training intervention open gap (Sep 04) now has a fifth failure mode to incorporate, and this one operates at a different layer (the guardrail, not the policy), suggesting that unified training may need to distinguish faithful reasoning from secure tool authorization.

## My Thoughts

<!-- Add your own notes here -->
