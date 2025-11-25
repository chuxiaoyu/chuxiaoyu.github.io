---
layout: default
title: Blogs
permalink: /blogs/
---

<div class="blog-page">
  {% if site.posts and site.posts != empty %}
  <ul class="blog-list">
    {% for post in site.posts %}
    <li class="blog-list-item">
      <div>
        <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
        {% if post.date %}
        <span class="blog-date">{{ post.date | date: "%B %-d, %Y" }}</span>
        {% endif %}
        <p class="blog-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      </div>
    </li>
    {% endfor %}
  </ul>
  {% else %}
  <p>No blog posts yet. Check back soon!</p>
  {% endif %}
</div>

