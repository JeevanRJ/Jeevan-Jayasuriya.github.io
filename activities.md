---
layout: archive
title: "Activities"
permalink: /activities/
---

{% include base_path %}

{% for post in site.activities reversed %}
  {% include archive-single-activity.html %}
{% endfor %}
