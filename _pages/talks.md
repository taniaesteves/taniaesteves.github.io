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
<h2 class="talks-year">{{ group.name }}</h2>
<div class="talks-group">
{% for item in group.items %}
<div class="talk" data-year="{{ item.year }}" data-type="{{ item.type | slugify }}">
<p>
    <span class="talk__type talk__type--{{ item.type | slugify }}">{{ item.type }}</span>
    <span style="color:#063c72"><strong>{{ item.title }}</strong><br></span>
    {{ item.venue }}.<br>
    {% if item.location %}{{ item.location }}.<br>{% endif %}
    {% if item.slides %}<a href="{{ item.slides }}"><i class="fas fa-fw fa-tv zoom"></i></a>{% endif %}
</p>
</div>
{% endfor %}
</div>
{% endfor %}


## Posters
<hr/>

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
