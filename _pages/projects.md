---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% for proj in site.data.projects %}

### <span style="color:#063c72">{% if proj.acronym %}{{ proj.acronym }}: {% endif %}{{ proj.title }}</span>
**{{ proj.role }}**<br>
{{ proj.date_start }} -- {% if proj.date_end %}{{ proj.date_end }}{% else %}Present{% endif %}<br>
{%- if proj.description -%}
  {{ proj.description }}<br>
{%- endif -%}
{%- if proj.partners -%}**Partners:** {% for partner in proj.partners %}<a href="{{ partner.url }}" target="_blank">{{ partner.name }}</a>{% if forloop.last == false %}, {% endif %}{% endfor %}<br>{%- endif -%}
{%- if proj.reference -%}**Reference:** {{ proj.reference }}<br>{%- endif -%}
{%- if proj.website -%}**Website:** <a href="{{proj.website}}">{{ proj.website }}</a>{%- endif -%}

{% endfor %}
