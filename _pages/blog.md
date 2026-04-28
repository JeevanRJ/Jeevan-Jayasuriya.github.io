---
layout: archive
title: "Blog"
permalink: /blog/
author_profile: true
---

<style>
.blog-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 25px;
}

.blog-card {
  border: 1px solid #e0e0e0;
  border-radius: 12px;
  padding: 20px;
  background: #ffffff;
  box-shadow: 0 4px 10px rgba(0,0,0,0.05);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.blog-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 18px rgba(0,0,0,0.1);
}

.blog-title {
  font-size: 20px;
  font-weight: 600;
  margin-bottom: 10px;
}

.blog-excerpt {
  font-size: 14px;
  color: #555;
  margin-bottom: 15px;
}

.read-more {
  text-decoration: none;
  color: white;
  background: #007acc;
  padding: 8px 14px;
  border-radius: 6px;
  font-size: 14px;
  transition: background 0.2s ease;
}

.read-more:hover {
  background: #005f99;
}
</style>

<div class="blog-container">
{% for post in site.posts %}
  <div class="blog-card">
    <div class="blog-title">{{ post.title }}</div>
    <div class="blog-excerpt">{{ post.excerpt }}</div>

    <a href="{{ post.url }}" target="_blank" class="read-more">
      Read More →
    </a>
  </div>
{% endfor %}
</div>
