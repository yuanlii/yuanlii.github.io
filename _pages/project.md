---
layout: archive
permalink: /DS project/
title: "Data Science Project"
author_profile: true
header:
    image: "/images/brenna-huff-OzKgJ5BP5vU-unsplash.jpg"
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