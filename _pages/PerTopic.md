---
layout: single
classes: wide
permalink: /Pertopic/
title: "Per Topic"
author_profile: true
header:
  image: "/images/desert.jpg"
  image_description: "High Fens, Belgium"
  caption: "Photo credit: [**Juliette Forest**](https://julietteforest.com)"
---



{% include base_path %}
{% include group-by-array collection=site.posts field="tags" %}

{% for tag in group_names %}
  {% assign posts = group_items[forloop.index0] %}
  <h2 id="{{ tag | slugify }}" class="archive__subtitle">{{ tag }}</h2>
  {% for post in posts %}
    {% include archive-single.html %}
  {% endfor %}
{% endfor %}
