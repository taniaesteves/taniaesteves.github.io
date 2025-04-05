---
layout: archive
title: "Software"
permalink: /software/
author_profile: true
---

{% for tool in site.data.software %}
<h3><span style="color:#063c72"><a href="{{ tool.git }}">{{ tool.name }}</a></span></h3>
{{ tool.description }}<br>
{% if tool.git %}<a href="{{ tool.git }}"><i class="fas fa-fw fa-laptop-code zoom"></i></a>{% endif %}
{% if tool.website %}<a href="{{ tool.website }}"><i class="fas fa-fw fa-globe zoom"></i></a>{% endif %}
<hr>
{% endfor %}
