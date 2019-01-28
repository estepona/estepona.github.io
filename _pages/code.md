---
title: "code"
permalink: /code/
layout: archive
author_profile: true
---

111001101010001010100110

{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% if tag == "code" %}
    {% assign posts = group_items[forloop.index0] %}
    <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
    {% for post in posts %}
        {% include archive-single.html %}
    {% endfor %}
  {% endif %}
{% endfor %}