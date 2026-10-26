---
layout: page
title: ML Playground
description: Shared ML benchmarks and an agent that learns from experiment results.
permalink: /projects/ml_playground/
importance: 1
category: personal
---

Implemented a shared preprocessing and benchmarking framework for classification, regression and forecasting, covering tree-based methods, neural networks and specialized foundation models for tabular data and time series. Models use common evaluation splits for direct comparison on the same dataset.

Added an agent that inspects dataframes, proposes predictive tasks and uses these tools to test hypotheses, diagnose results and revise its approach. Evaluated local Qwen3.8-27B with xhigh reasoning on four datasets: building energy, bike sharing, wearable activity and finance.

**Finding:** Iteration brought limited, inconsistent gains beyond the first benchmark. On reserved data, bike demand prediction improved, finance retained its initial model, and energy and activity performance worsened.

[Code](https://github.com/oremaz/ml-playground)
