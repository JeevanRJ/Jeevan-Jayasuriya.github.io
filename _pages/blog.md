---
layout: archive
title: "Blog"
permalink: /blog/
author_profile: true
---

{% for post in site.posts %}
  <h2>{{ post.title }}</h2>
  <p>{{ post.excerpt }}</p>

  <a href="{{ post.url }}" target="_blank">Read more</a>

  <hr>
{% endfor %}
