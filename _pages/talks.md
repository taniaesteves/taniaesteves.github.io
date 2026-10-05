---
layout: archive
title: "Talks"
permalink: /talks/
author_profile: true
display_categories: ["2023", "2022", "2019"]
horizontal: false
---

{% assign talks_by_year = site.data.talks | group_by: "year" | sort: "name" | reverse %}
{% for group in talks_by_year %}
<h2>{{ group.name }}</h2>
<div class="talks-group">
{% for item in group.items %}
<div class="entry talk" data-year="{{ item.year }}" data-type="{{ item.type | slugify }}">
<p>
    <span class="type-badge type-badge--{{ item.type | slugify }}">{{ item.type }}</span>
    <span class="entry__title">{{ item.title }}</span><br>
    {{ item.venue }}.<br>
    {% if item.location %}{{ item.location }}.{% endif %}
</p>
{% if item.slides or item.url %}<div class="pub__links">
  {%- if item.slides %}<a class="pub__btn" href="{{ item.slides }}"><i class="fas fa-tv"></i> Slides</a>{% endif -%}
  {%- if item.url %}<a class="pub__btn" href="{{ item.url }}"><i class="fas fa-calendar-alt"></i> Event</a>{% endif -%}
</div>{% endif %}
</div>
{% endfor %}
</div>
{% endfor %}


## Posters

<div class="post">
    <article>
        <div class="posters">
            <!-- Display posters without categories -->
            {%- assign sorted_posters = site.posters | sort: "importance" -%}
            <!-- Generate cards for each poster -->
            <div class="grid">
                {%- for poster in sorted_posters -%}
                {% include poster.html %}
                {%- endfor %}
            </div>
        </div>
    </article>
</div>
