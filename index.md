---
layout: default
---

<div class="post-grid">
  {% for post in site.posts %}
    <a href="{{ post.url | relative_url }}" class="post-tile">
      <div class="post-content">
        <h3>{{ post.title }}</h3>
        <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
        <p>{{ post.excerpt | strip_html | truncatewords: 20 }}</p>
      </div>
    </a>
  {% endfor %}
</div>
