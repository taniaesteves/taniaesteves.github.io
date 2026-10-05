---
layout: archive
title: "Supervision"
permalink: /supervision/
author_profile: true
---

{% assign sections = "PhD|PhD Theses,MSc|MSc Theses" | split: "," %}
{% for section in sections %}
{% assign s = section | split: "|" %}
## {{ s[1] }}

{% assign my_array = site.data.supervision | where: "type", s[0] %}
{% for item in my_array %}
<div class="entry">
<p>
    <span class="entry__meta">{% include date-range.html start=item.start_date end=item.end_date %}</span>
    <span class="entry__title">{{ item.title }}</span><br>
    <strong>{{ item.students }}</strong><br>
    <span class="entry__detail">{{ item.venue }}{% if item.advisors %}. {{ item.advisors | markdownify | remove: '<p>' | remove: '</p>' | strip }}{% endif %}.</span>
</p>
</div>
{% endfor %}
{% endfor %}

## Research Mentoring

{% assign my_array = site.data.supervision | where: "type", "Mentoring" %}
{% for item in my_array %}
<div class="entry">
<p>
    <span class="entry__meta">{% include date-range.html start=item.start_date end=item.end_date %}</span>
    <span class="entry__title">{{ item.title }}</span><br>
    {{ item.students | markdownify | remove: '<p>' | remove: '</p>' | strip }}<br>
    {% if item.advisors %}<span class="entry__detail">{{ item.advisors | markdownify | remove: '<p>' | remove: '</p>' | strip }}.</span>{% endif %}
</p>
</div>
{% endfor %}

## Academic / Scientific Projects

{% assign my_array = site.data.supervision | where: "type", "Academic Project" %}
{% for item in my_array %}
<div class="entry">
<p>
    <span class="entry__meta">{% include date-range.html start=item.start_date end=item.end_date %}</span>
    <span class="entry__title">{{ item.title }}</span><br>
    {{ item.students | markdownify | remove: '<p>' | remove: '</p>' | strip }}<br>
    <span class="entry__detail">{{ item.project }}, {{ item.class }}, {{ item.venue }}.{% if item.advisors %} {{ item.advisors | markdownify | remove: '<p>' | remove: '</p>' | strip }}.{% endif %}</span>
</p>
</div>
{% endfor %}
