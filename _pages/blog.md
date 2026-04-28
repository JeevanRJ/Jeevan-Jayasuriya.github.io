---
layout: archive
title: "Blog"
permalink: /blog/
author_profile: true
---

<style>
/* 🌐 Page container */
.blog-wrapper {
  max-width: 1050px;
  margin: auto;
  padding: 20px;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Arial;
}

/* 🧠 Header controls */
.blog-controls {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
  margin-bottom: 60px;
}

/* 🔍 Search bar (modern) */
#searchInput {
  flex: 1;
  padding: 14px 16px;
  border-radius: 12px;
  border: 1px solid #e5e5e5;
  font-size: 15px;
  outline: none;
  transition: 0.2s;
}

#searchInput:focus {
  border-color: #007acc;
  box-shadow: 0 0 0 3px rgba(0,122,204,0.1);
}

/* 📊 Sort dropdown */
#sortSelect {
  padding: 14px 14px;
  border-radius: 12px;
  border: 1px solid #e5e5e5;
  font-size: 14px;
  background: white;
}

/* 📦 Grid layout */
.blog-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 22px;
}

/* 🧊 Modern card */
.blog-card {
  background: #ffffff;
  border-radius: 16px;
  padding: 20px;
  border: 1px solid #f0f0f0;
  box-shadow: 0 6px 20px rgba(0,0,0,0.04);
  transition: all 0.25s ease;
}

/* hover animation */
.blog-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 12px 30px rgba(0,0,0,0.08);
}

/* 🏷 Title */
.blog-title {
  font-size: 18px;
  font-weight: 650;
  margin-bottom: 6px;
  color: #111;
}

/* 📅 Date */
.blog-date {
  font-size: 13px;
  color: #888;
  margin-bottom: 12px;
}

/* 📝 excerpt */
.blog-excerpt {
  font-size: 14px;
  color: #555;
  line-height: 1.5;
  margin-bottom: 16px;
}

/* 🔗 button */
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

/* 📱 mobile fix */
@media (max-width: 600px) {
  .blog-controls {
    flex-direction: column;
  }
}
</style>

<div class="blog-wrapper">

  <!-- 🔍 Controls -->
  <div class="blog-controls">
    <input type="text" id="searchInput" placeholder="Search articles...">

    <select id="sortSelect">
      <option value="latest">Latest</option>
      <option value="oldest">Oldest</option>
    </select>
  </div>

  <!-- 📚 Blog grid -->
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
// 🔍 search
const searchInput = document.getElementById("searchInput");
const cards = document.querySelectorAll(".blog-card");

searchInput.addEventListener("input", function () {
  const value = this.value.toLowerCase();

  cards.forEach(card => {
    card.style.display = card.innerText.toLowerCase().includes(value)
      ? "block"
      : "none";
  });
});

// 📊 sort
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
