---
layout: archive
title: "Activities"
permalink: /_activities/
author_profile: true
---

{% include base_path %}

{% for post in site.activities reversed %}
  {% include archive-single-activity.html %}
{% endfor %}
