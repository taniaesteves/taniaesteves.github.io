---
layout: archive
title: "Talks"
permalink: /talks/
author_profile: true
display_categories: ["2023", "2022", "2019"]
horizontal: false
---

## Conference talks
<hr/>

{% assign my_array = site.data.talks | where: "type", "Conference" %}
{% for item in my_array %}
<div class="talk">
<p>
    <span style="color:#063c72"><strong>{{ item.title }}</strong><br></span>
    {{ item.venue }}.<br>
    {{ item.location }}. {{ item.year }}.<br>
    {% if item.slides %}<a href="{{ item.slides }}"><i class="fas fa-fw fa-tv zoom"></i></a>{% endif %}
</p>
</div>
{% endfor %}


## Workshop talks
<hr/>

{% assign my_array = site.data.talks | where: "type", "Workshop" %}
{% for item in my_array %}
<div class="talk">
<p>
    <span style="color:#063c72"><strong>{{ item.title }}</strong><br></span>
    {{ item.venue }}.<br>
    {{ item.location }}. {{ item.year }}.<br>
    {% if item.slides %}<a href="{{ item.slides }}"><i class="fas fa-fw fa-tv zoom"></i></a>{% endif %}
</p>
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

## Others
<hr/>

{% assign my_array = site.data.talks | where: "type", "Other" %}
{% for item in my_array %}
<div class="talk">
<p>
    <span style="color:#063c72"><strong>{{ item.title }}</strong><br></span>
    {{ item.venue }}.<br>
    {{ item.location }}. {{ item.year }}.<br>
    {% if item.slides %}<a href="{{ item.slides }}"><i class="fas fa-fw fa-tv zoom"></i></a>{% endif %}
    </p>
</div>
{% endfor %}
