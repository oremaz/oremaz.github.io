---
layout: page
title: AI Content Detection & Watermarking
description: Benchmarking detection, adaptive evasion and watermark removal for text and images.
permalink: /projects/ai_content_robustness/
importance: 2
category: personal
---

Built a workbench to study AI-content detection, generator adaptation and detector retraining.

- **Text detection:** Trained classical baselines and QLoRA classifiers on a MAGE subset, then evaluated cross-dataset transfer. The Qwen3.5-4B classifier achieved **92.36% accuracy on MAGE, 83.10% on AI Text Detection Pile and 81.40% on an external peer-review benchmark**, showing uneven generalization.
- **Image detection:** Trained on ArtiFact, a collection of real images and synthetic images from multiple generators. EfficientNet reached **93.76% accuracy on the ArtiFact holdout but 50.00% on CIFAKE**, exposing poor cross-dataset transfer.
- **Adaptive evasion:** Fine-tuned **Qwen3.5-9B-Base** against individual detectors and an ensemble while monitoring semantic similarity. Ensemble evasion reached **94.8%**, then fell to **0.4% after one detector update** on new attack outputs. Detection of original-model outputs remained **98.4%**, down from 100%. These results concern a fixed attacker, not another adaptive round. Image experiments apply the same attack–retrain question to **Stable Diffusion 1.5**.
- **Watermarking (ongoing):** Integrated Meta’s **TextSeal with Qwen3.5-4B-Base** and released **DistSeal checkpoints for RAR-XL and UViT-H/DC-AE**. Evaluating detection, output quality and removal when the watermark scheme is unknown, with or without original clean weights. Removal uses merging or clean-data training; the owner’s detector is used afterward for evaluation, without exposing its weights, secrets or scores to training.

[Code](https://github.com/oremaz/ai-content-robustness)
