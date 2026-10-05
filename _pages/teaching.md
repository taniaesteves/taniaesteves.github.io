---
layout: archive
title: "Teaching"
permalink: /teaching/
author_profile: true
---

{% assign t = site.data.teaching %}
{% assign first_year = "" %}
{% for c in t.courses %}{% assign y = c.years | first %}{% if first_year == "" or y < first_year %}{% assign first_year = y %}{% endif %}{% endfor %}

<p class="teaching__role">
  <strong>{{ t.position }}</strong> · {{ t.institution }} · {{ first_year | split: "/" | first }} – present
</p>

{% for c in t.courses %}
{% assign y0 = c.years | first %}
{% assign y1 = c.years | last %}
<div class="teaching__course">
<p>
    <span class="teaching__years">{{ y0 | split: "/" | first }}/{{ y0 | split: "/" | last | slice: 2, 2 }}{% if y0 != y1 %} – {{ y1 | split: "/" | first }}/{{ y1 | split: "/" | last | slice: 2, 2 }}{% endif %}</span>
    {% assign main_title = c.title_pt | default: c.title %}
    <span style="color:#063c72"><strong>{% if c.url %}<a href="{{ c.url }}">{{ main_title }}</a>{% else %}{{ main_title }}{% endif %}</strong>{% if c.acronym %} ({{ c.acronym }}){% endif %}</span>
    {% if c.title_pt %}<span class="teaching__alt">· {{ c.title }}</span>{% endif %}<br>
    {{ c.class }}<br>
    {{ c.type | default: "Practical classes" }}<br>
    {% if c.note %}<span class="teaching__note">{{ c.note }}</span>{% endif %}
</p>
</div>
{% endfor %}

<p class="teaching__see-also">
  See also: <a href="{{ '/supervision/' | relative_url }}">student supervision</a>.
</p>
