---
title: "Aha Moment Revisited: Are VLMs Truly Capable of Self Verification in Inference-time Scaling?"
authors: ["Mingyuan Wu", "Meitang Li", "Jingcheng Yang", "Jize Jiang", "Kaizhuo Yan", "Zhaoheng Li", "Hanchao Yu", "Minjia Zhang", "Klara Nahrstedt"]
date: 2026-07-15
arxiv_id: "2506.17417"
url: "http://arxiv.org/abs/2506.17417v3"
score: 0.88
topics: [multimodal models, vision language models, VLM, agentic RL, RL training, RLAIF]
status: unread
---

# Aha Moment Revisited: Are VLMs Truly Capable of Self Verification in Inference-time Scaling?

## Summary

Tests whether RL-trained VLMs benefit from inference-time self-verification the way LLMs do; finds that simple majority voting consistently and substantially outperforms verification-centric strategies like best-of-N with self-verification in VLMs. Visual information is not effectively integrated into the self-verification process of current RL-trained VLMs, and behaviors like the 'Aha moment' do not yield reliable reasoning improvements across visual modalities. This directly challenges the assumption that the RL verifier co-training thread (Tango, PAG, SVR-R1) transfers seamlessly to visual modality inference-time gains.

## Key Contributions

- Extensive evaluation showing majority voting beats best-of-N with self-verification for RL-tuned VLMs on visual math reasoning
- Documents that visual information is not effectively integrated into VLM self-verification: the model's verbal self-check does not faithfully reflect visual evidence
- Shows the 'Aha moment' behavior observed in text RL models does not yield reliable inference-time improvements in VLMs
- Identifies a fundamental VLM/LLM asymmetry: generation-time capability matters more than verification for VLMs, opposite to the text-model picture

## Relevance

Directly answers the question queued in the Jul 14 digest about SVR-R1's decreasing-reliance pattern: VLM self-verification does not generalize to inference-time scaling in the visual modality, creating a gap between text-LLM (Tango, PAG) and VLM (SVR-R1) verifier co-training. The vault's verifier co-training thread is now: closed for text LLMs, partially open for VLMs — SVR-R1 shows training-time gains, this paper shows inference-time gains do not follow.

## My Thoughts

<!-- Add your own notes here -->
