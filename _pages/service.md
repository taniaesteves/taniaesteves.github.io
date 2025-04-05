---
layout: archive
title: "Service"
permalink: /service/
author_profile: true
---

{% assign service_list = site.data.service | group_by: "type" %}
{% for type_list in service_list %}
<h2><span style="color:#063c72">{{ type_list.name }}</span></h2>
<hr>
{% for service in type_list.items %}
**{{ service.year }}** - {{ service.venue }} ([{{ service.acronym }}]({{ service.website }})) {% if service.additional_info %}{{ service.additional_info }}{% endif %}<br>
{% endfor %}
{% endfor %}
