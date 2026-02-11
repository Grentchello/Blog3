---
layout: default
---

<style>
  /* Reuse the grid and card styles from before */
  .category-section { margin-bottom: 40px; }
  .category-title { 
    border-bottom: 2px solid #0366d6; 
    padding-bottom: 10px; 
    margin-bottom: 20px; 
    text-transform: capitalize;
  }
  .post-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 20px;
  }
  .post-card {
    background: #fff;
    border: 1px solid #e1e4e8;
    border-radius: 12px;
    padding: 20px;
    text-decoration: none !important;
    color: #24292e !important;
    display: block;
    transition: transform 0.2s;
  }
  .post-card:hover { transform: translateY(-4px); box-shadow: 0 4px 12px rgba(0,0,0,0.1); }
</style>

<div class="category-section">
  <h2 class="category-title">Books</h2>
  <div class="post-grid">
    {% for post in site.categories.book %}
      <a href="{{ post.url | relative_url }}" class="post-card">
        <h3>{{ post.title }}</h3>
        <p>{{ post.excerpt | strip_html | truncatewords: 15 }}</p>
      </a>
    {% endfor %}
  </div>
</div>

<div class="category-section">
  <h2 class="category-title">Movies</h2>
  <div class="post-grid">
    {% for post in site.categories.movie %}
      <a href="{{ post.url | relative_url }}" class="post-card">
        <h3>{{ post.title }}</h3>
        <p>{{ post.excerpt | strip_html | truncatewords: 15 }}</p>
      </a>
    {% endfor %}
  </div>
</div>
