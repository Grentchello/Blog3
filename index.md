---
layout: default
---

# Welcome to my Blog!

I'll be posting updates on my **C# projects**, **vehicle dynamics simulations**, and **astrophotography** here. 


Check out my latest posts below:

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

