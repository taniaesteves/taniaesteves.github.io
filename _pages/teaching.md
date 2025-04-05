---
layout: archive
title: "Teaching"
permalink: /teaching/
author_profile: true
---
{% assign uc_list = site.data.teaching | group_by: "year" %}
{% for year_list in uc_list %}
<h2>{{ year_list.name }}</h2>
<hr>
{% for uc in year_list.items %}
### <span style="color:#063c72">{{ uc.title }}</span>
**{{ uc.position }}**<br>
{{uc.class}}<br>
{% endfor %}
{% endfor %}
