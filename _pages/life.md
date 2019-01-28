---
title: "life"
permalink: /life/
layout: archive
author_profile: true
---

{% include group-by-array collection=site.posts field="tags" %}

<!-- {% for tag in group_names %}
  <p> {{ group_name }}, {{ tag }}</p>
  {% if tag == title %}
    {% assign posts = group_items[forloop.index0] %}
    {% for post in posts %}
      {% include archive-single.html %}
    {% endfor %}
  {% endif %}
{% endfor %} -->

{% assign posts = group_items[forloop.index0] %}
{% for post in posts %}
  <p> {{title}} {{group_names[tag]}}</p>
  {% if title in group_names[tag] %}
    {% include archive-single.html %}
  {% endif %}
{% endfor %}