---
layout: default
---

<style>
  .post-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 20px;
    padding: 20px 0;
  }

  .post-card {
    background: #ffffff;
    border: 1px solid #e1e4e8;
    border-radius: 12px;
    padding: 20px;
    text-decoration: none !important; /* Prevents default link underline */
    color: #24292e !important;
    transition: all 0.2s ease-in-out;
    display: flex;
    flex-direction: column;
    box-shadow: 0 2px 4px rgba(0,0,0,0.05);
  }

  .post-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 16px rgba(0,0,0,0.1);
    border-color: #0366d6;
  }

  .post-title {
    margin: 0 0 10px 0;
    font-size: 1.25rem;
    color: #0366d6;
  }

  .post-date {
    font-size: 0.85rem;
    color: #586069;
    margin-bottom: 12px;
  }

  .post-excerpt {
    font-size: 0.95rem;
    line-height: 1.5;
    color: #444;
  }
</style>

# Books

<div class="post-grid">
  {% for post in site.posts %}
    <a href="{{ post.url | relative_url }}" class="post-card">
      <h3 class="post-title">{{ post.title }}</h3>
      <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
      <p class="post-excerpt">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
    </a>
  {% endfor %}
</div>

