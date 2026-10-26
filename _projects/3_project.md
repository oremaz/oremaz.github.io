---
layout: page
title: NutriCoach — Nutrition Assistant
description: A conversational app for meal planning, nutrition tracking and recipe analysis.
permalink: /projects/nut_agent/
importance: 3
category: personal
---

Built a Streamlit assistant to help users plan meals and track progress toward their nutrition goals. The app runs locally on macOS and supports free hosted LLMs or local inference when hardware permits.

- **Set up a profile:** Enter personal goals to calculate calorie and macronutrient targets. Chat with the assistant to create and save meal plans.
- **Track daily intake:** Log meals, water and weight, then review nutrition totals and trends. Upload a food photo to estimate portions and nutrients, review or correct the estimates, and save the meal.
- **Explore recipes:** Enter a recipe or compare two side by side to estimate preparation time, difficulty and meal type, with optional LLM-based nutrition analysis.

- **Food vision, integrated into the app:** Developed and compared approaches for estimating meal portions, calories and macronutrients from food photos, and integrated this work directly into NutriCoach’s photo-analysis workflow.

LangGraph tools handle calculations, food lookups and logging, while persistent profiles and journals maintain context across sessions. Nutrition estimates remain editable.

[Code](https://github.com/oremaz/nutricoach)
