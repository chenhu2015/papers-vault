---
title: "Evolve Vision-Language-Action Model into an Agent with On-the-fly Tool-use"
authors: ["Yi Ding", "Yanzhao Yu", "Xili Dai", "Xianbiao Qi", "Peiwen Sun", "Xueqian Wang", "Xiangyu Yue", "Jianan Wang"]
date: 2026-08-14
arxiv_id: "2608.14047"
url: "https://arxiv.org/abs/2608.14047"
score: 0.84
topics: [vision-language, VLM, tool use, agentic, multimodal models]
status: unread
---

# Evolve Vision-Language-Action Model into an Agent with On-the-fly Tool-use

## Summary

ART (Agentic Robot with Tool-use) is a tool-injection framework that augments any VLA model with on-the-fly use of off-the-shelf tool modules for low-level vision, affordance estimation, and embodiment enhancement. By replacing a continuous action solution space with modular tool calls, ART reduces data dependency to 30K trajectories — far smaller than baseline requirements — while achieving a 20% higher success rate on challenging pick-and-place tasks in novel viewpoints and low-light conditions.

## Key Contributions

- Tool-injection architecture: any VLA model can call off-the-shelf tool modules for vision, affordance, and embodiment without retraining the backbone
- Solution space compression: modular tool use discretizes and reduces the continuous action space, improving generalizability under distribution shift
- Data efficiency: 30K tool-use trajectories vs. much larger baselines achieve 20% higher task success
- Robustness demonstration: novel viewpoints and low-light pick-and-place, where visual feature tools substitute for backbone generalization

## Relevance

ART is the VLA-side instantiation of the core interest profile's VLM + agentic + tool use intersection. The Explicit Language Memory paper (Aug 18) addressed long-horizon VLA via hierarchical decoupling; ART addresses it via tool injection that preserves the VLA backbone while adding agentic capabilities. Together they represent two strategies for extending VLA models into the agentic regime without retraining from scratch.

## My Thoughts

<!-- Add your own notes here -->
