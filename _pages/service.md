---
layout: archive
title: "Service"
permalink: /service/
author_profile: true
---

{% assign categories = "Organization & Chairing|Program Committees|Artifact Evaluation Committees|Journal Reviewing" | split: "|" %}
{% for category in categories %}
{% assign items = site.data.service | where: "type", category %}
{% if items.size > 0 %}
## {{ category }}

{% for service in items %}
{% assign label = service.acronym | default: service.venue %}
<div class="entry entry--compact">
<p>
    <span class="entry__meta">{{ service.years | join: ", " }}</span>
    <span class="entry__title">{% if service.website %}<a href="{{ service.website }}">{{ label }}</a>{% else %}{{ label }}{% endif %}</span>{% if service.acronym %} — {{ service.venue }}{% endif %}{% if service.note %} <span class="entry__detail">{{ service.note }}</span>{% endif %}
</p>
</div>
{% endfor %}
{% endif %}
{% endfor %}
