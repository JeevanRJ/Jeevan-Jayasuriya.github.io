---
layout: archive
title: "Blog"
permalink: /blog/
author_profile: true
---

<style>
.blog-wrapper {
  max-width: 1100px;
  margin: auto;
  padding: 10px;
}

/* Top controls (search + sort) */
.blog-controls {
  display: flex;
  gap: 10px;
  margin-bottom: 20px;
  flex-wrap: wrap;
}

/* Search */
#searchInput {
  flex: 1;
  padding: 10px;
  border-radius: 8px;
  border: 1px solid #ccc;
}

/* Sort dropdown */
#sortSelect {
  padding: 10px;
  border-radius: 8px;
  border: 1px solid #ccc;
}

/* Grid */
.blog-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
}

/* Card */
.blog-card {
  border-radius: 12px;
  padding: 18px;
  background: #ffffff;
  box-shadow: 0 4px 12px rgba(0,0,0,0.06);
  transition: all 0.25s ease;
}

.blog-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 22px rgba(0,0,0,0.12);
}

.blog-title {
  font-size: 18px;
  font-weight: 600;
  margin-bottom: 5px;
}

.blog-date {
  font-size: 13px;
  color: #888;
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
  padding: 7px 12px;
  border-radius: 6px;
  font-size: 13px;
}

.read-more:hover {
  background: #005f99;
}

/* 🌙 Dark mode */
@media (prefers-color-scheme: dark) {
  .blog-card {
    background: #1e1e1e;
    color: #eaeaea;
  }

  .blog-excerpt {
    color: #bbb;
  }

  .blog-date {
    color: #999;
  }

  #searchInput, #sortSelect {
    background: #2a2a2a;
    color: white;
    border: 1px solid #444;
  }
}
</style>

<div class="blog-wrapper">

  <!-- Controls -->
  <div class="blog-controls">
    🔍 <input type="text" id="searchInput" placeholder="Search blog posts...">
    
    📊 
    <select id="sortSelect">
      <option value="latest">Latest</option>
      <option value="oldest">Oldest</option>
    </select>
  </div>

  <div class="blog-container" id="blogList">
  {% for post in site.posts %}
    <div class="blog-card" data-date="{{ post.date | date: '%s' }}">
      
      <div class="blog-title">{{ post.title }}</div>

      <div class="blog-date">
        {{ post.date | date: "%B %d, %Y" }}
      </div>

      <div class="blog-excerpt">{{ post.excerpt }}</div>

      <a href="{{ post.url }}" target="_blank" class="read-more">
        Read More →
      </a>
    </div>
  {% endfor %}
  </div>

</div>

<script>
// 🔍 Search
const searchInput = document.getElementById("searchInput");
const cards = document.querySelectorAll(".blog-card");

searchInput.addEventListener("keyup", function() {
  const value = this.value.toLowerCase();

  cards.forEach(card => {
    const text = card.innerText.toLowerCase();
    card.style.display = text.includes(value) ? "block" : "none";
  });
});

// 📊 Sorting
const sortSelect = document.getElementById("sortSelect");
const container = document.getElementById("blogList");

sortSelect.addEventListener("change", function() {
  const cardsArray = Array.from(container.children);

  cardsArray.sort((a, b) => {
    const dateA = parseInt(a.getAttribute("data-date"));
    const dateB = parseInt(b.getAttribute("data-date"));

    return this.value === "latest" ? dateB - dateA : dateA - dateB;
  });

  // Re-append sorted cards
  cardsArray.forEach(card => container.appendChild(card));
});
</script>
