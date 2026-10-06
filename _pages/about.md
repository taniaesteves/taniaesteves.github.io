---
permalink: /
title: "About me"
hide_title: true
# excerpt: "About me"
layout: archive
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

I am an Assistant Researcher at [INESC TEC](https://www.inesctec.pt/en) ([DSR HASLab](https://dsr-haslab.github.io/) group) and an Invited Assistant Professor at [University of Minho](https://www.uminho.pt/EN).
My research focuses on diagnosing and benchmarking distributed and data-centric applications, as well as enhancing systems security and data privacy.

Much of my recent work builds on [eBPF](https://ebpf.io), both to observe and diagnose systems with low overhead and to extend eBPF itself for performance tuning and security.

## News

{% include news-list.html limit=5 %}
{% if site.data.news.size > 5 %}<p class="news__more"><a href="{{ '/news/' | relative_url }}">All news →</a></p>{% endif %}

## Selected Publications

{% bibliography --query @*[selected=true] %}
<p class="news__more"><a href="{{ '/publications/' | relative_url }}">All publications →</a></p>

## Ongoing Projects

{% assign selected_projects = site.data.projects | where: "selected", true %}
{% for proj in selected_projects %}
<div class="entry entry--compact">
<p>
    <span class="entry__meta">{% include date-range.html start=proj.date_start end=proj.date_end %}</span>
    <span class="entry__title">{% if proj.website %}<a href="{{ proj.website }}">{{ proj.acronym | default: proj.title }}</a>{% else %}{{ proj.acronym | default: proj.title }}{% endif %}</span>{% if proj.acronym %} — {{ proj.title }}{% endif %}
</p>
</div>
{% endfor %}
<p class="news__more"><a href="{{ '/projects/' | relative_url }}">All projects →</a></p>
