---
title: "π-Play: Multi-Agent Self-Play via Privileged Self-Distillation without External Data"
authors: ["Yaocheng Zhang", "Yuanheng Zhu", "Wenyue Chong", "Songjun Tu", "Qichao Zhang", "Jiajun Chai", "Xiaohan Wang", "Wei Lin", "Guojun Yin", "Dongbin Zhao"]
date: 2026-04-15
arxiv_id: "2604.14054v1"
url: "http://arxiv.org/abs/2604.14054v1"
score: 0.77
topics: [agentic RL, RL training, LLM agent]
status: unread
---

# π-Play: Multi-Agent Self-Play via Privileged Self-Distillation without External Data

## Summary

π-Play discovers that the Question Construction Path (QCP) produced during self-play task generation is a privileged artifact capturing the reverse solution process—and leverages it to transform conventional sparse-reward self-play into a dense-feedback loop. An examiner generates tasks along with their QCPs; a teacher uses QCP as privileged context to densely supervise a student via self-distillation, eliminating the credit assignment problem inherent in sparse terminal rewards. Data-free π-Play surpasses fully supervised search agents and improves evolutionary efficiency 2–3× over conventional self-play.

## Key Contributions

- QCP (Question Construction Path) as a source of privileged information: zero-cost, high-quality dense supervision naturally generated during self-play
- Teacher-student distillation loop that uses QCP context to guide the student without external data or human feedback
- Transforms sparse-outcome self-play into dense-feedback self-evolution with 2–3× efficiency gain
- Outperforms fully supervised search agents despite requiring no external data

## Relevance

Directly addresses the sparse reward / credit assignment problem in agentic RL—the same family of problems as StePPO and ProceedRL from earlier digests—but via a self-play mechanism rather than learned critics. The insight that task-generation artifacts are themselves rich supervision signals is a novel angle on dense reward construction.

## My Thoughts

<!-- Add your own notes here -->
