---
title: "Posts"
permalink: "/posts/"
layout: default
---

{% if site.show_excerpts %}
  {% include home.html %}
{% else %}
  {% include archive.html title="Posts" %}
{% endif %}
