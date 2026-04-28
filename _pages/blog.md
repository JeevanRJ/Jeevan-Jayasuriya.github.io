---
layout: archive
title: "Blog"
permalink: /blog/
author_profile: true
---

{% for post in site.posts %}
  <div style="margin-bottom: 30px;">
    <h2>{{ post.title }}</h2>
    <p>{{ post.excerpt }}</p>

    <a href="{{ post.url }}" target="_blank" style="color: blue;">
      Read more →
    </a>
  </div>
{% endfor %}
