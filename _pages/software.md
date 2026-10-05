---
layout: archive
title: "Software"
permalink: /software/
author_profile: true
---

{% for tool in site.data.software %}
<div class="entry">
<p>
    <span class="entry__meta">
        {% if tool.git %}<a href="{{ tool.git }}" title="Code"><i class="fas fa-fw fa-laptop-code zoom"></i></a>{% endif %}
        {% if tool.website %}<a href="{{ tool.website }}" title="Website"><i class="fas fa-fw fa-globe zoom"></i></a>{% endif %}
    </span>
    <span class="entry__title">{% if tool.git %}<a href="{{ tool.git }}">{{ tool.name }}</a>{% else %}{{ tool.name }}{% endif %}</span><br>
    {{ tool.description }}
</p>
</div>
{% endfor %}
