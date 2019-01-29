---
title: "code"
permalink: /categories/code/
layout: archive
author_profile: true
---

{% for post in site.categories.code %}
  {% include archive-single.html show_read_time=true %}
{% endfor %}