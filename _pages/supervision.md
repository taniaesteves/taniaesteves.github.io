---
layout: archive
title: "Supervision"
permalink: /supervision/
author_profile: true
---

## PhD Theses
<hr/>

{% assign my_array = site.data.supervision | where: "type", "PhD" %}
{% for item in my_array %}
{{ item.start_date }}{% if item.end_date %} - {{ item.end_date }}{% else %} (ongoing){% endif %}. **{{ item.students }}**. <span style="color:#063c72">**{{ item.title }}**.</span><br>{{ item.venue }}. {{ item.advisors }}.
{% endfor %}

## MSc Theses
<hr/>

{% assign my_array = site.data.supervision | where: "type", "MSc" %}
{% for item in my_array %}
{{ item.start_date }}{% if item.end_date %} -- {{ item.end_date }}{% else %} (ongoing){% endif %}. **{{ item.students }}**. <span style="color:#063c72">**{{ item.title }}**.</span><br>{{ item.venue }}. {{ item.advisors }}.
{% endfor %}


## Other Supervision Activities
<hr/>

### Research Mentoring
<hr/>

{% assign my_array = site.data.supervision | where: "type", "Mentoring" %}
{% for item in my_array %}
{{ item.start_date }}{% if item.end_date %} - {{ item.end_date }}{% else %} (ongoing){% endif %}. <span style="color:#063c72">**{{ item.title }}**.</span><br> {{ item.students }}.{% if item.advisors %}<br>{{ item.advisors }}.{% endif %}
{% endfor %}


### Academic / Scientific projects
<hr/>

{% assign my_array = site.data.supervision | where: "type", "Academic Project" %}
{% for item in my_array %}
{{ item.start_date }}{% if item.end_date %} - {{ item.end_date }}{% else %} (ongoing){% endif %}. <span style="color:#063c72">**{{ item.title }}**.</span><br> {{ item.students }}.<br>{{ item.project }}.<br>{{ item.class }}.<br>{{ item.venue }}.{% if item.advisors %} {{ item.advisors }}.{% endif %}
{% endfor %}
