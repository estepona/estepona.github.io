---
title: "life"
permalink: /life/
layout: archive
author_profile: true
---

<!-- {% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  <p> {{ group_name }}, {{ tag }}</p>
  {% if tag == title %}
    {% assign posts = group_items[forloop.index0] %}
    {% for post in posts %}
      {% include archive-single.html %}
    {% endfor %}
  {% endif %}
{% endfor %} -->

{% for post in site.categories.life %}
 <li><span>{{ post.date | date_to_string }}</span> &nbsp; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}