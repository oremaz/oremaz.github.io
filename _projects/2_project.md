---
layout: page
title: AI Content Detection & Watermarking
description: Benchmarking detection, adaptive evasion and watermark removal for text and images.
permalink: /projects/ai_content_robustness/
importance: 2
category: personal
---

Built a workbench to study AI-content detection, generator adaptation and detector retraining.

- **Text and image detection:** Benchmarked classical baselines and QLoRA on MAGE, where Qwen3.5-4B achieved 92.36% accuracy versus 83.10% on AI Text Detection Pile and 81.40% on an external peer-review benchmark. For images, EfficientNet dropped from 93.76% on the ArtiFact holdout to 50.00% on CIFAKE.
- **Adaptive evasion:** Fine-tuned Qwen3.5-9B-Base with GRPO (LoRA) against individual detectors and an ensemble while monitoring semantic similarity. Ensemble evasion reached 94.8%, then fell to 0.4% after one detector update on new attack outputs. Detection of original-model outputs remained 98.4%, down from 100%. Image experiments apply the same attack–retrain question to Stable Diffusion 1.5 using DDPO.
- **Watermarking:** Evaluated Meta’s TextSeal 2 on Qwen3.5-4B-Instruct and adapted DistSeal’s watermark distillation to the same language model. An adaptive attack removed TextSeal 2 while meeting the quality criterion on 95/128 prompts. For images, clean LoRA fine-tuning reduced DistSeal detection from 100% to 4.9% on RAR-XL and 0.2% on UViT-H/DC-AE.

[Code](https://github.com/oremaz/ai-content-robustness)
