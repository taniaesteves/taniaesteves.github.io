---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

{% assign ongoing = site.data.projects | where_exp: "p", "p.date_end == nil" %}
{% assign past = site.data.projects | where_exp: "p", "p.date_end != nil" %}
{% assign sections = "Ongoing|Past" | split: "|" %}
{% for section in sections %}
{% if section == "Ongoing" %}{% assign list = ongoing %}{% else %}{% assign list = past %}{% endif %}
## {{ section }}

{% for proj in list %}
<div class="entry">
<p>
    <span class="entry__meta">{% include date-range.html start=proj.date_start end=proj.date_end %}</span>
    <span class="entry__title">{% if proj.website %}<a href="{{ proj.website }}">{{ proj.acronym | default: proj.title }}</a>{% else %}{{ proj.acronym | default: proj.title }}{% endif %}</span>{% if proj.acronym %} — {{ proj.title }}{% endif %}<br>
    {% if proj.description %}{{ proj.description }}<br>{% endif %}
    {%- assign bits = "" | split: "" -%}
    {%- if proj.typology -%}{%- assign bits = bits | push: proj.typology -%}{%- endif -%}
    {%- if proj.reference -%}{%- assign ref = "Ref. " | append: proj.reference -%}{%- assign bits = bits | push: ref -%}{%- endif -%}
    {%- if proj.partners -%}
      {%- capture partners -%}Consortium: {% for partner in proj.partners %}{% if partner.url %}<a href="{{ partner.url }}">{{ partner.name }}</a>{% else %}{{ partner.name }}{% endif %}{% unless forloop.last %}, {% endunless %}{% endfor %}{%- endcapture -%}
      {%- assign bits = bits | push: partners -%}
    {%- endif %}
    {% if bits.size > 0 %}<span class="entry__detail">{{ bits | join: " · " }}</span><br>{% endif %}
    {% if proj.role %}{% assign role_lc = proj.role | downcase %}{% if role_lc contains 'coordinator' %}<span class="project__role project__role--coordinator"><i class="fas fa-flag"></i> {{ proj.role }}</span>{% else %}<span class="project__role"><i class="fas fa-user"></i> {{ proj.role }}</span>{% endif %}{% endif %}
</p>
</div>
{% endfor %}
{% endfor %}
