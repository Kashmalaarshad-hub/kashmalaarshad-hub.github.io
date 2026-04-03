---
layout: default
title: Blog
permalink: /blog/
---

<div class="blog-page">
  <div class="blog-header">
    <h1>📖 My Blog</h1>
    <p>Weekly reflections, lab notes, and CE journey posts 🌸</p>
  </div>

  {% for post in site.posts %}
  <a href="{{ post.url | relative_url }}" class="post-card">
    <div class="post-card-meta">
      <span class="tag">{{ post.categories | first | default: "Blog" }}</span>
      <span class="post-date">{{ post.date | date: "%B %d, %Y" }}</span>
    </div>
    <h2>{{ post.title }}</h2>
    <p>{{ post.excerpt | strip_html | truncate: 160 }}</p>
    <span class="read-more">Read more →</span>
  </a>
  {% endfor %}

  {% if site.posts.size == 0 %}
  <p style="color: var(--text-light); text-align: center; margin-top: 40px;">No posts yet — coming soon! 🌸</p>
  {% endif %}
</div>
