---
title: "GTR-Turbo: Merged Checkpoint is Secretly a Free Teacher for Agentic VLM Training"
authors: ["Tong Wei", "Yijun Yang", "Changhao Zhang", "Junliang Xing", "Yuanchun Shi", "Zongqing Lu", "Deheng Ye"]
date: 2026-07-02
arxiv_id: "2512.13043v2"
url: "https://arxiv.org/abs/2512.13043"
score: 0.83
topics: [agentic RL, VLM, multimodal models, tool use, vision-language, LLM agent]
status: unread
---

# GTR-Turbo: Merged Checkpoint is Secretly a Free Teacher for Agentic VLM Training

## Summary

GTR-Turbo eliminates dependence on expensive teacher VLMs in multi-turn agentic RL by merging checkpoints produced during ongoing RL training and using the merged model as a 'free' teacher for subsequent RL via SFT or soft logit distillation. This design prevents entropy collapse observed in prior dense-reward methods and reduces wall-clock training time by 50% and compute by 60% compared to GTR, while improving baseline accuracy by 10–30% on diverse visual agentic tasks.

## Key Contributions

- Checkpoint merging during RL training creates a self-improving teacher without any external privileged model (GPT/Gemini)
- Teacher guides subsequent RL via supervised fine-tuning or soft logit distillation on step-level feedback
- Addresses entropy collapse observed in prior guided thought reinforcement work
- 50% wall-clock reduction, 60% compute reduction vs. GTR; 10–30% accuracy improvement over baseline on visual agentic tasks

## Relevance

GTR-Turbo closes the VLM agentic RL gap that "Why Does RL Generalize Better Than SFT?" (Jul 1) opened: that paper showed RL's generalization advantage is data-selective rather than algorithmic, implying that RL-distilled data pipelines might be replaceable. GTR-Turbo confirms this direction for VLM agents — merging RL checkpoints to extract a cheap teacher is exactly the offline curation analog for the agentic setting. The paper also connects to the SWITCH (Jun 30) and self-distillation threads: the merged checkpoint acts as a latent-reasoning surrogate by aggregating diverse intermediate RL policy states.

## My Thoughts

<!-- Add your own notes here -->
