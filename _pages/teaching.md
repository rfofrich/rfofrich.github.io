---
layout: page
title: Teaching
permalink: /teaching/
description: Courses taught and assisted, with brief descriptions.
nav: true
nav_order: 4
---

<!-- pages/teaching.md -->
<div class="teaching">
{% assign sorted_teachings = site.teachings | sort: "order" %}
{% for course in sorted_teachings %}
  <div class="teaching-entry" style="margin-bottom: 2rem;">
    <h3>{{ course.title }}</h3>
    <p style="margin-bottom: 0.5rem;"><em>{{ course.role }}</em>, {{ course.institution }} ({{ course.years }})</p>
    <p>{{ course.content }}</p>
  </div>
{% endfor %}
</div>
