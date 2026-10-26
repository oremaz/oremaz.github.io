---
layout: page
title: projects
permalink: /projects/
description: Personal experiments in machine learning, robustness and LLM agents.
nav: true
nav_order: 3
---

{% assign projects = site.projects | sort: 'importance' %}
{% for project in projects %}

## [{{ project.title }}]({{ project.url | relative_url }})

{{ project.content }}
{% endfor %}
