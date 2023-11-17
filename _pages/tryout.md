---
layout: page
title: tryout
permalink: /tryout/
description: A growing collection of your cool tryout.
nav: true
nav_order: 2
display_categories: [work, fun]
horizontal: false
---

<!-- pages/tryout.md -->
<div class="tryout">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized tryout -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_tryout = site.tryout | where: "category", category -%}
  {%- assign sorted_tryout = categorized_tryout | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_tryout -%}
      {% include tryout_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_tryout -%}
      {% include tryout.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display tryout without categories -->
  {%- assign sorted_tryout = site.tryout | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_tryout -%}
      {% include tryout_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_tryout -%}
      {% include tryout.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>