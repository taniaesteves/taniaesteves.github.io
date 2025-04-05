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
{{ proj.description }}<br>{% if proj.partners %}**Partners:** {{ proj.partners }}<br>{% endif %}{% if proj.reference %}**Reference:** {{ proj.reference }}<br>{% endif %}{% if proj.website %}**Website:** <a href="{{proj.website}}">{{ proj.website }}</a>{% endif %}
{% endfor %}
