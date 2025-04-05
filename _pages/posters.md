---
layout: page
title: posters
permalink: /posters/
description: A growing collection of your cool projects.
author_profile: false
display_categories: ["2023", "2022", "2019"]
horizontal: false
---

<!-- pages/posters.md -->
<div class="posters">
{%- if site.enable_poster_categories and page.display_categories %}
  <!-- Display categorized posters -->
  {%- for category in page.display_categories %}
  <h3 class="category">{{ category }}</h3>
  {%- assign categorized_posters = site.posters | where: "category", category -%}
  {%- assign sorted_posters = categorized_posters | sort: "importance" %}
  <!-- Generate cards for each poster -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for poster in sorted_posters -%}
      {% include poster_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for poster in sorted_posters -%}
      {% include poster.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display posters without categories -->
  {%- assign sorted_posters = site.posters | sort: "importance" -%}
  <!-- Generate cards for each poster -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for poster in sorted_posters -%}
      {% include poster_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for poster in sorted_posters -%}
      {% include poster.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>