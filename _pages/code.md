---
title: "code"
permalink: /code/
layout: archive
author_profile: true
---

111001101010001010100110

{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% if tag == page.title %}
    {% assign posts = group_items[forloop.index0] %}
    {% for post in posts %}
        {% include archive-single.html %}
    {% endfor %}
  {% endif %}
{% endfor %}