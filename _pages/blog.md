---
layout: archive
title: "Blog"
permalink: /blog/
author_profile: true
---

<style>
.blog-wrapper {
  max-width: 1050px;
  margin: auto;
  padding: 20px;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Arial;
}

/* 📊 Sort controls */
.blog-controls {
  display: flex;
  justify-content: flex-end;
  margin-bottom: 60px;
}

#sortSelect {
  padding: 14px;
  border-radius: 12px;
  border: 1px solid #e5e5e5;
  font-size: 14px;
  background: white;
}

/* 📦 Grid */
.blog-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 22px;
}

/* 🧊 Card */
.blog-card {
  background: #ffffff;
  border-radius: 16px;
  padding: 20px;
  border: 1px solid #f0f0f0;
  box-shadow: 0 6px 20px rgba(0,0,0,0.04);
  transition: all 0.25s ease;
}

.blog-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 12px 30px rgba(0,0,0,0.08);
}

/* Title */
.blog-title {
  font-size: 18px;
  font-weight: 650;
  margin-bottom: 6px;
  color: #111;
}

/* Date */
.blog-date {
  font-size: 13px;
  color: #888;
  margin-bottom: 12px;
}

/* Excerpt */
.blog-excerpt {
  font-size: 14px;
  color: #555;
  line-height: 1.5;
  margin-bottom: 16px;
}

/* Button */
.read-more {
  display: inline-block;
  text-decoration: none;
  color: white;
  background: #007acc;
  padding: 8px 14px;
  border-radius: 10px;
  font-size: 13px;
  transition: 0.2s ease;
}

.read-more:hover {
  background: #005f99;
}

/* Mobile */
@media (max-width: 600px) {
  .blog-controls {
    justify-content: center;
  }
}
</style>

<div class="blog-wrapper">

  <!-- 📊 Sort only -->
  <div class="blog-controls">
    <select id="sortSelect">
      <option value="latest">Latest</option>
      <option value="oldest">Oldest</option>
    </select>
  </div>

  <!-- 📚 Blog cards -->
  <div class="blog-container" id="blogList">

  {% for post in site.posts %}
    <div class="blog-card" data-date="{{ post.date | date: '%s' }}">

      <div class="blog-title">{{ post.title }}</div>

      <div class="blog-date">
        {{ post.date | date: "%B %d, %Y" }}
      </div>

      <div class="blog-excerpt">
        {{ post.excerpt }}
      </div>

      <a href="{{ post.url }}" target="_blank" class="read-more">
        Read article →
      </a>

    </div>
  {% endfor %}

  </div>

</div>

<script>
// 📊 Sorting only
const sortSelect = document.getElementById("sortSelect");
const container = document.getElementById("blogList");

sortSelect.addEventListener("change", function () {
  const items = Array.from(container.children);

  items.sort((a, b) => {
    const da = parseInt(a.dataset.date);
    const db = parseInt(b.dataset.date);

    return this.value === "latest" ? db - da : da - db;
  });

  items.forEach(item => container.appendChild(item));
});
</script>
